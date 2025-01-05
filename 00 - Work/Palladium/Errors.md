
### Varios usuarios Pre Registrados con mismo email (no ocurrira pero por si acaso)  
statusCode:409  
[  
    {  
        "message": "There is many email pre registered Agents",  
        "errorCode": "Conflict",  
        "agentData": null,  
        "agencyData": null  
    }  
]  

Email no existe como usuario Pre Registrado  
  statusCode:404  
[  
    {  
        "message": "Agent Email was not found in the system",  
        "errorCode": "Not Found",  
        "agentData": null,  
        "agencyData": null  
    }  
]

### Codigo Agencia (Iata o Loyalty ID) no existe en la base de datos

statusCode:206  
[  
    {  
        "message": "Agency was not found in the system",  
        "errorCode": "Partial Content",  
        "agentData": {  
            "transferPointsRewards": null,  
            "status": null,  
            "shippingAddress": {  
                "state": null,  
                "postalCode": null,  
                "country": "AF",  
                "city": null,  
                "address": null  
            },  
            "prefix": null,  
            "position": null,  
            "personBirthdate": null,  
            "newsletters": null,  
            "mobilePhone": null,  
            "memberReferalCode": null,  
            "loyaltyIdPalladiumPro": null,  
            "lastName": "saddsa",  
            "language": null,  
            "isResponsibleAgent": null,  
            "idRewards": null,  
            "flagAgreeRegisterB2C": null,  
            "firstName": "sdsad",  
            "email": "seidor0000@yopmail.com",  
            "documentType": null,  
            "documentNumber": null,  
            "academyId": null  
        },  
        "agencyData": null  
    }  
]


### Respuestas Servicio GetAgencyByCode  
Varios usuarios Pre Registrados con mismo email (no ocurrira pero por si acaso)  
statusCode:409  
[  
    {  
        "message": "There is many email pre registered Agents",  
        "errorCode": "Conflict",  
        "agentData": null,  
        "agencyData": null  
    }  
]  


statusCode:200  
[  
    {  
        "message": null,  
        "errorCode": null,  
        "agentData": {  
            "transferPointsRewards": null,  
            "status": null,  
            "shippingAddress": {  
                "state": null,  
                "postalCode": null,  
                "country": "AF",  
                "city": null,  
                "address": null  
            },  
            "prefix": null,  
            "position": null,  
            "personBirthdate": null,  
            "newsletters": null,  
            "mobilePhone": null,  
            "memberReferalCode": null,  
            "loyaltyIdPalladiumPro": null,  
            "lastName": "saddsa",  
            "language": null,  
            "isResponsibleAgent": null,  
            "idRewards": null,  
            "flagAgreeRegisterB2C": null,  
            "firstName": "sdsad",  
            "email": "seidor0000@yopmail.com",  
            "documentType": null,  
            "documentNumber": null,  
            "academyId": null  
        },  
        "agencyData": {  
            "fiscalData": {  
                "status": "Pre",  
                "shippingAddress": {  
                    "state": "Madrid",  
                    "postalCode": "ES",  
                    "country": "ES",  
                    "city": "Madrid",  
                    "address": "alguna"  
                },  
                "prefix": "+34",  
                "phone": "649765389",  
                "fiscalName": "PApruebas Fiscal",  
                "email": "papruebas@tesmail.com",  
                "cif": "H88976"  
            },  
            "businessData": {  
                "webPage": "[https://huakai.es/"](https://huakai.es/%22 "https://huakai.es/%22"),  
                "shippingAddress": {  
                    "state": "Madrid",  
                    "postalCode": "28234",  
                    "country": "ES",  
                    "city": "Madrid",  
                    "address": null  
                },  
                "idIATA": "ES21",  
                "businessName": "Agencia PApruebas",  
                "agencyLoyaltyId": "240288765"  
            }  
        }  
    }  
]

### Email no existe como usuario Pre Registrado  
  statusCode:404  
[  
    {  
        "message": "Agent Email was not found in the system",  
        "errorCode": "Not Found",  
        "agentData": null,  
        "agencyData": null  
    }  
]

### Codigo Agencia (Iata o Loyalty ID) no existe en la base de datos

statusCode:206  
[  
    {  
        "message": "Agency was not found in the system",  
        "errorCode": "Partial Content",  
        "agentData": {  
            "transferPointsRewards": null,  
            "status": null,  
            "shippingAddress": {  
                "state": null,  
                "postalCode": null,  
                "country": "AF",  
                "city": null,  
                "address": null  
            },  
            "prefix": null,  
            "position": null,  
            "personBirthdate": null,  
            "newsletters": null,  
            "mobilePhone": null,  
            "memberReferalCode": null,  
            "loyaltyIdPalladiumPro": null,  
            "lastName": "saddsa",  
            "language": null,  
            "isResponsibleAgent": null,  
            "idRewards": null,  
            "flagAgreeRegisterB2C": null,  
            "firstName": "sdsad",  
            "email": "seidor0000@yopmail.com",  
            "documentType": null,  
            "documentNumber": null,  
            "academyId": null  
        },  
        "agencyData": null  
    }  
]

200 -> Success

206 -> Partial Success No se encuentra a la agencia (antiguo 404) pero si al AGENTE

404: ->ERROR Not Found (no se encuentra AL AGENTE)

409 -> ERROR (no deberia ocurrir pero por si acaso)