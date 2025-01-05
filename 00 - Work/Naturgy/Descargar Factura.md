
Al cargar la pagina hacer primera llamada con el InvoiceNumber y el Token

	```
https://www.naturgy.es/descarga_tu_factura?invoiceNumber=FE21321352522515&token=54e5566bf087d24ec64aae090081e9cd27a112b15648872989a582b3f3f906c7%7C849CCC34134478CED9A718CF48DA9C56D33B0609
```

```
http://rovcon.intranet.gasnatural.com/ovh-web/APMUserInvoiceAccess.gas?invoiceNumber=FE21321352522515&document=null&mode=validateInvoice
```

Al dar click en descargar factura abrir modal para ingresar el DNI y hacer llamada a

```
http://rovcon.intranet.gasnatural.com/ovh-web/APMUserInvoiceAccess.gas?invoiceNumber=FE21321352522515&document=Y0575093S&mode=validateNif
```

Si el DNI es valido, hacer una llamada a enviando el DNI

```
http://rovcon.intranet.gasnatural.com/ovh-web/DownloadInvoiceFol.gas?invoiceNumber=FE21321352522515&token=54e5566bf087d24ec64aae090081e9cd27a112b15648872989a582b3f3f906c7%7C849CCC34134478CED9A718CF48DA9C56D33B0609&language=es&utm_source=AREACLIENTE-NuevaFOL&utm_medium=email&utm_campaign=AREACLIENTE&dni=Y0575093S
```


```
http://rovcon.intranet.gasnatural.com/ovh-web/APMUserInvoiceAccess.gas
```

Enlace Caudcado

```
https://www.naturgy.es/descarga_tu_factura?invoiceNumber=FE21321352522515&token=54e5566bf087d24ec64aae090081e9cd27a112b15648872989a582b3f3f906c7%7C849CCC34134478CED9A718CF48DA9C56D33B0609
```


```
https://areaprivada.naturgy.es/ovh-web/v1/FOLClientService.gas?token=54e5566bf087d24ec64aae090081e9cd27a112b15648872989a582b3f3f906c7%7C849CCC34134478CED9A718CF48DA9C56D33B0609&invoiceNumber=FE21321352522515
```
### Responses

Puedes introducir el DNI
```json
{
    "result": {
        "CodResult": "RESULT_45",
        "MsgResult": "Debes introducir NIF para poder continuar"
    }
}
```

DNI Erroneo
```json
{
    "result": {
        "CodResult": "RESULT_47",
        "MsgResult": "El NIF introducido no es válido, por favor, vuelve a intentarlo"
    }
}
```

DNI Correcto
```json
{
    "result": {
        "CodResult": "RESULT_00",
        "MsgResult": "No hay error"
    }
}
```

IP Bloqueada
```json
{
    "result": {
        "CodResult": "RESULT_48",
        MsgResult: "Si necesitas ayuda para acceder a tu factura puedes contactar con Atención al Cliente. Teléfono 900 100 251, de lunes a sábado de 8:00 a 22:00 horas. Muchas gracias y disculpa las molestias."
    }
}
```


Token caducado
```json
{
    "result": {
        "codResult": "RESULT_S18_03",
        "msgResult": "El token de la factura ha caducado"
    }
}
```

DNI
```
Y0575093S
```


http://rovcon.intranet.gasnatural.com/ovh-web/FOLClientService.gas?invoiceNumber=FE21321352522515&document=null&mode=validateInvoice