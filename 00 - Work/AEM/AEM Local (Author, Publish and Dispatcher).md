# Guía para Instalar AEM Author, Publish y Dispatcher en Mac (Sin Docker)

Esta guía te ayudará a configurar instancias de AEM **Author**, **Publish** y un **Dispatcher** en tu Mac sin usar Docker.

---

## **1. Requisitos previos**

Asegúrate de tener los siguientes elementos antes de empezar:

1. **Java Development Kit (JDK):**
   - Descarga e instala la versión de JDK compatible con tu versión de AEM (Java 8 o 11).
   - Verifica la instalación:
```bash
 java -version
```

2. **Paquete de AEM:**
   - Obtén los archivos de instalación de **AEM Quickstart Jar** desde el portal oficial de Adobe.

3. **Acceso al Dispatcher:**
4. 
   - Descarga el módulo Dispatcher correspondiente desde el portal de Adobe.

---

## **2. Configurar AEM Author y Publish**

### 2.1 Preparar los archivos

1. Coloca el archivo `aem-quickstart.jar` en un directorio de tu elección.

2. Crea carpetas separadas para las instancias Author y Publish:
 
```bash
mkdir ~/aem-author ~/aem-publish
```

3. Copia el archivo aem-quickstart.jar en cada carpeta y renómbralo para diferenciarlos:

```
~/aem-author/aem-author.jar
```

```
~/aem-publish/aem-publish.jar
```

### 2.2 Configurar los puertos

1. Dentro de cada carpeta, crea un archivo `start` para iniciar las instancias:

**Para Author:**
   
```bash
#!/bin/bash
java -jar aem-author.jar -r author -p 4502
```

**Para Publish:**

```bash
#!/bin/bash
java -jar aem-publish.jar -r publish -p 4503
```

2. Otorga permisos de ejecución a los scripts:

```bash
   chmod +x ~/aem-author/start ~/aem-publish/start  
```

## **2.3 Iniciar las instancias**

Ejecuta las instancias en terminales separadas:

```
cd ~/aem-author && ./start
cd ~/aem-publish && ./start
```

Verifica el funcionamiento accediendo a las URLs:

• **Author:** [http://localhost:4502](http://localhost:4502)

• **Publish:** [http://localhost:4503](http://localhost:4503)

## **3. Configurar el Dispatcher**

### 3.1 Instalar Apache HTTP Server

1. Instala Apache HTTP Server usando **Homebrew**:

```bash
brew install httpd
```

2. Verifica que Apache esté funcionando:

```bash
sudo apachectl start
open http://localhost
```

### 3.2 Descargar Dispatcher

1. Descarga el módulo Dispatcher desde el portal de Adobe.

2. Copia el archivo del módulo a la carpeta de módulos de Apache:

```bash
sudo cp dispatcher-apache*.so /usr/local/etc/httpd/modules
```

### 3.3 Configurar Dispatcher

1. Edita el archivo httpd.conf para cargar el módulo Dispatcher:

```bash
sudo nano /usr/local/etc/httpd/httpd.conf
```

Agrega esta línea:

```apache
LoadModule dispatcher_module /usr/local/etc/httpd/modules/dispatcher-apache*.so
```

2. Crea un archivo de configuración básico para Dispatcher llamado dispatcher.any:

```apache
/farms {
  /farm1 {
    /clientheaders {
      "Referer"
      "User-Agent"
    }
    /virtualhosts {
      "localhost*"
    }
    /renders {
      /rend01 {
        /hostname "localhost"
        /port "4503" # Dirección de la instancia Publish
      }
    }
  }
}
```

3. Vincula el archivo de configuración en httpd.conf:

```apache
<IfModule dispatcher_module>
    DispatcherConfig /usr/local/etc/httpd/dispatcher.any
    DispatcherLog /usr/local/var/log/httpd/dispatcher.log
    DispatcherLogLevel 3
</IfModule>
```

4. Reinicia Apache para aplicar los cambios:

```bash
sudo apachectl restart
```

5. Verifica que Dispatcher redirija correctamente a la instancia Publish accediendo a:

• [http://localhost](http://localhost)


## **4. Verificación final**

• **AEM Author:** [http://localhost:4502](http://localhost:4502)

• **AEM Publish:** [http://localhost:4503](http://localhost:4503)

• **Dispatcher:** [http://localhost](http://localhost)

