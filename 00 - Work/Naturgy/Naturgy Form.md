
FormData

```json
{
  "subject": "Hello, World!",
  "ngyMails": "[\"email1@example.com\",\"email2@example.com\"]",
  "to": "email@example.com",
  "username": "test de sistemas",
  "body": {
    "Código Anterior Consulta": "test",
    "Detalla el motivo de tu consulta": "esto es un test de sistemas",
    "Nombre y apellidos/ Razón Social": "test de sistemas",
    "Número de documento": "08824286Z",
    "Teléfono": "666666666",
    "Horario Contacto": "test de sistemas",
    "Email (en el que recibirás respuesta)": "djcacheiro@viewnext.com",
    "Dirección sobre la que deseas solicitar el trámite": "test de sistemas",
    "¿Eres cliente?": "option2 - No soy cliente",
    "Selecciona el motivo": "Otros motivos",
    "Tipo de documento": "NIF"
  }
}
```

PROD

```
https://www.naturgy.pt/pt/grandes_clientes/produtos/mobilidade_sustentavel/mobilidade_GNV_
```

```
https://www.naturgy.pt/pt/grandes_clientes/ajuda_e_contato/atendimento_ao_cliente#formulario
```

```
https://www.naturgy.es/Form_Atencion_Cliente
```

Responsive Container
```
<div data-sly-resource="${'responsivegrid' @ resourceType='wcm/foundation/components/responsivegrid'}"></div>
```

ERROR
```json
{
  "errors": [
    {
      "response": "ko",
      "error": "Null"
    }
  ],
  "response": []
}
```

```json
{
  "errors": [
    {
      "response": "ko",
      "error": "No selectors provided"
    }
  ],
  "response": []
}
```

SUCCESS
```json
{
  "errors": [],
  "response": [
    {
      "Service Response": ""
    }
  ]
}
```