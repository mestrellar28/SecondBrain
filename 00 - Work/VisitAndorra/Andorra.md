
# Convenciones de Nombres

1. **Componentes**: `kebab-case`
2. **ClientLibs**: `clientlib-kebab-case`
3. **Modelos**: `CapitalCase` o `CapitalCasePojo` (ej. `ProductoModel`, `ProductoModelPojo`)
4. **Servicios**: `CapitalCaseService` (ej. `ProductoService`)
5. **Servlets**: `CapitalCaseServlet` (ej. `ProductoServlet`)
6. **Endpoints Internos**: `/bin/generico/especifico.selector.json`
    - Ejemplos:
        - `/bin/forms/send.basic.json`
        - `/bin/tiendas/lists.json`

---
# Estructura BACK

- 📂 configurations
- 📂 filters
- 📂 listeners
- 📂 models
    - 📂 components
        - 📂 componentname
    - 📂 form
        - 📂 componentname
    - 📂 renditions
    - 📂 structure
        - 📂 componentname
- 📂 pojos
- 📂 components
    - 📂 componentname
- 📂 form
    - 📂 componentname
- 📂 renditions
- 📂 structure
    - 📂 componentname
- 📂 schedulers
    - 📂 components
        - 📂 componentname
    - 📂 form
        - 📂 componentname
    - 📂 structure
        - 📂 componentname
- 📂 services
    - 📂 servicename
        - 📂 impl
            - 📄 ServiceNameServiceImpl
        - 📄 ServiceNameService
- 📂 servlets
    - 📂 components
- 📂 migrations
- 📂 structure
- 📂 utils
    - 📂 commons
    - 📂 connection
    - 📂 constants
- 📂 workflow

---
# Estructura HTML

- 📂 visitaandorra
    - 📂 clientlibs
        - 📂 clientlib-base
        - 📂 clientlib-grid
    - 📂 components
        - 📂 commons
            - 📂 component-name
        - 📂 core
            - 📂 component-name
        - 📂 structure
            - 📂 content-page
        - 📂 utils
            - 📂 dialog
            - 📂 templates
    - 📂 i18n

---
# Estructura FRONT

- 📂 **site**
	- 📂 javascript
	    - 📂 components
	        - 📄 component-name.js
	    - 📂 utils
	        - 📄 util.js
	- 📂 styles
	    - 📂 base
	    - 📂 components
	        - 📄 component-name.scss
	    - 📂 layout
	    - 📂 modules
	    - 📂 partials
	    - 📂 settings
	    - 📂 utilities
	    - 📂 pluggins

---
# Guía Rápida de Estándares de Programación

## Espaciado y Sangría

- **Tab Width**: 4 espacios.
- **Estructura Modular**: Considerar siempre que una página puede contener uno o varios componentes.

## Evitar

- **Bootstrap** y **jQuery**.

## Estándares por Entorno

### **Back-End**

- **Uso de corchetes en estructuras de control**:

  ```java
  if ("a") {
      // lógica
  } else {
      // lógica alterna
  }
  ```

### **HTML**

- **Sintaxis Semántica**:

  ```html
  ${properties.value @ i18n}
  ${properties.value @ context='html'}
  ```

### **Front-End**

- **CSS**

  - **Unidades**: Preferir `rem` y `em` sobre `px`.

  - **Ejemplos de Buenas y Malas Prácticas**:

❌ BAD

```scss
    .sticky-banner-tarifas {
        &__title {
            &__text {
                // estilos
            }
        }
        &__text {
            // estilos
        }
    }
```


✅ GOOD

```scss
    .sticky-banner-tarifas {
        color: blue;
        
        @media (min-width: @tablet) {
            color: red;
        }

        .sticky-banner-tarifas__title {
            .sticky-banner-tarifas__title__text {
                // estilos
            }
        }

        .sticky-banner-tarifas__text {
            // estilos
        }
    }
```



- **JavaScript**

  - **Declaración de variables**: Usar `let` y `const` en lugar de `var`.

  - **Estructura de control**:

```javascript
    if (condition) {
        // lógica
    } else {
        // lógica alterna
    }
```

  - **Funciones**:

```javascript
    function exampleFunction() {
        // lógica
    }
```

---
# Diálogos Comunes en Utils de HTML

Los siguientes diálogos representan propiedades comunes en múltiples componentes y están organizados dentro de la carpeta `utils` para HTML.

### **Propiedades Reutilizables**

- **Enlace**
  - `DropdownEstilo`
  - `Texto`
  - `Icono`
  - `Link`
  - `CTA`

- **RichText**
  - `Color`
  - `Párrafos/Encabezados (h1, h2, etc.)`
  - `Tablas`

- **Imagen**
  - `src`
  - `alt`
  - `Link`
  - `Lazy (checkeado)`

---
# Componentes Comunes
## Contenedor General (Container)

- **Componentes**:
  - Crear un componente de tipo `container` que permita seleccionar el fondo, el cual puede ser:
    - **Imagen**
    - **Color**
    - **Gradiente**
  - Este contenedor debe estructurarse como un elemento `section`.
  - A nivel general, el contenedor principal debe ser un elemento `main` para mejorar la semántica y la estructura del sitio.
## Botón

- **Funcionalidad**: Puede abrir un modal. Si se usa esta opción, debe incluir un `data-target` que indique el ID del modal.
- **Estructura**:

  ```html
  <button>
      <span class="icon"><!-- Icono aquí --></span>
      <span class="text">Texto del botón</span>
  </button>
  ```

## Enlace

- **Estructura**:

  ```html
  <a href="#">
      <span class="icon"><!-- Icono aquí --></span>
      <span class="text">Texto del enlace</span>
  </a>
  ```

## Modales

- **Uso**: Utilizar un componente de modal que solo contenga los eventos y estilos básicos de un modal. Este componente debe tener un ID y actuar como un contenedor (`container`), sin lógica adicional.

## Slider

- **Consideraciones**: Configuración pendiente (Manu está revisando).

## Formularios

- **Directrices**: 
  - Evitar el uso de frameworks completos.
  - Crear formularios individuales que aprovechen utilidades genéricas, lo que facilita el mantenimiento.

## Tabs

- **Consideraciones**: Consultar con Sergio.

## Slides

- **Configuración**:
  - Implementar una grid para mejorar la contribución y permitir una visualización clara en el modo `view as publish`.
  - Personalización de color para las flechas de navegación y los puntos indicadores.

## Posicionamiento y Visualización de Componentes

- **Posicionamiento**: No dejar un componente vacío sin `position: relative` para que siempre sea visible y fácil de contribuir en su ubicación.
- **Cajetilla**: Incluir la cajetilla de la plantilla si no es posible añadir una contribución de forma predeterminada.

## Loader para Servicios

- **Esqueleto de carga**: Implementar un esqueleto de carga para los servicios mientras cargan.
  - Ejemplo visual:
    ![Esqueleto de carga](https://media.nngroup.com/media/editor/2023/05/18/headspace_skeletonscreenfull.png)

## Espaciado de Textos

- **RichText**: Unificar los espaciados en el componente RichText.

## Subtítulos + RichText

- **Distancias y Márgenes**: Hablar con Sergio sobre la mejor forma de manejar los subtítulos y el richtext, ya que los espacios pueden variar.

## Espaciado entre Componentes

- **Definición de Espaciado**: 
  - Usar el `StyleSystem` para aplicar márgenes.
  - Establecer un margen por defecto y permitir personalización adicional mediante el `StyleSystem` si es necesario.

## Tags para Eventos

- **Organización**:
  - Crear tabs con cada componente y su correspondiente tag ya contribuidos.
  - Alternativamente, incluir un componente de selector de tags que actualice el componente de eventos en función de la tag seleccionada.

## Contribución de Iconos

- **Directriz**: Asegurarse de que los iconos se contribuyen como tales, y no como imágenes.

## Mapas

- **Carga Dinámica**: Configurar la carga de mapas a través de la configuración general.

---
# Style System

El **Style System** permite configurar rápidamente estilos visuales y estructurales en los componentes. A continuación se definen las propiedades clave:

- **Text Size**: Configuración de tamaños de texto estandarizados.
- **Colors**: Selección de colores para texto, bordes y otros elementos decorativos.
- **Background (BG)**: Opciones de fondo para los componentes, como colores sólidos, gradientes e imágenes.

### Style System para Visualizaciones

- **Columnas**: Definir la disposición del contenido en diferentes configuraciones:
  - 1 columna
  - 2 columnas
  - 3 columnas
  - Otras configuraciones según sea necesario.


---
# Imágenes y Videos

### Renditions

- Crear una plantilla de imagen (`template`) que contenga:
  - `src`
  - `alt`
  - Otras propiedades relevantes.
- Implementar una transformación automática para convertir cualquier imagen a formato **WEBP** si es necesario (por ejemplo, transformar automáticamente PNG a WEBP).
- **Formato de imagen**: Siempre utilizar **WEBP** para optimización y rendimiento.

### Componente de Imagen

- **Lazy Load**: Opción de carga diferida (`lazy load`) configurable.
- **No Lazy Load**: Opción de carga no diferida, contribuyente si es necesario.

### Componente de Video

- Implementar el **lazy load** para optimizar la carga y el rendimiento del sitio.

---
# i18n (Internacionalización)

- **Optimización de i18n**: Consultar con Sergio la forma más eficiente de implementar la internacionalización.
- **Literales en Componentes**: Al finalizar el desarrollo de un componente, asegurar que todos los literales estén configurados en i18n para facilitar la traducción.
- **Uso en JavaScript**: En lugar de usar literales en el código JS, emplear atributos `data-*` para almacenar valores que puedan ser utilizados en el código JavaScript de forma dinámica.
