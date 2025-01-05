# Agent Form Registration

### Code IATA

	Error Codigo Erroneo

```json
{  
  "error": {  
    "errorCode": 404,  
    "errorDateTime": "2024-03-21T11:36:32.265Z",  
    "errorMessage": "Not Found",  
    "errorDescription": "Agency was not found in the system"  
  }  
}
```

	Correcto

```json
{  
  "agency": {  
    "fiscalData": {  
      "status": "Pre",  
      "shippingAddress": {  
        "state": "Madrid",  
        "postalCode": "ES",  
        "country": "ES",  
        "city": "Madrid",  
        "address": null  
      },  
      "prefix": "+34",  
      "phone": "649765389",  
      "fiscalName": null,  
      "email": null,  
      "cif": null  
    },  
    "businessData": {  
      "webPage": "https://huakai.es/",  
      "shippingAddress": {  
        "state": "Madrid",  
        "postalCode": "28234",  
        "country": "ES",  
        "city": "Madrid",  
        "address": null  
      },  
      "idIATA": "ES22",  
      "businessName": "67TGF",  
      "agencyLoyaltyId": null  
    }  
  }  
}
```

### Loyalty ID

	Error

```json
{  
  "error": {  
    "errorCode": 404,  
    "errorDateTime": "2024-03-21T11:38:46.370Z",  
    "errorMessage": "Not Found",  
    "errorDescription": "Member was not found in the system"  
  }  
}
```

	Correcto

```json
{  
  "agency": {  
    "businessData": {  
      "webPage": "https://huakai.es/",  
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
    },  
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
    }  
  },  
  "agent": {  
    "transferPointsRewards": true,  
    "status": "Active",  
    "shippingAddress": {  
      "state": "Madrid",  
      "postalCode": "28234",  
      "country": "ES",  
      "city": "Madrid",  
      "address": "Calle Villa"  
    },  
    "prefix": "+34",  
    "position": "Agente",
    "points": {  
      "totalPointsBalanceValue": 0,  
      "totalPointsBalance": 0,  
      "totalPointsAccumulatedPintsValue": 0,  
      "totalPointsAccumulated": 0,  
      "rewardsConvertedPointsValue": 0,  
      "rewardsConvertedPoints": 0,  
      "pendingPointsValue": 0,  
      "pendingPoints": 0,  
      "multiplyPointsBy": 0  
    },  
    "personBirthdate": "1994-07-23",  
    "newsletters": true,  
    "mobilePhone": "938937263",  
    "memberReferalCode": "",  
    "lastName": "Prueba",  
    "language": "es",  
    "isResponsibleAgent": false,  
    "idRewards": "0lMVe00000003SXMAY",  
    "flagAgreeRegisterB2C": true,  
    "firstName": "Pau2",  
    "email": "paulocal1@email.test",  
    "documentType": "NIE",  
    "documentNumber": "34567832"  
  },  
  "hotels": [  
    {  
      "nameHotel": "Hotel 2"  
    },  
    {  
      "nameHotel": "Hotel 2"  
    }  
  ]  
}
```

### Send Agent Form

	Correcto

```json
{  
  "message": {  
    "code": "200",  
    "dateTime": "2024-03-21T11:40:09.485Z",  
    "description": "successful transaction"  
  }  
}
```

# Pre Registro

	 Success Correcto

```json
{  
    "message": {  
        "code": "201",  
        "dateTime": "2024-03-21T11:32:38.302Z",  
        "description": "successful transaction"  
    }  
}
```

	Error Correo Erroneo

```json
{  
    "error": {  
        "errorCode": 500,  
        "errorDateTime": "2024-03-21T11:32:17.365Z",  
        "errorMessage": "APEX_ERROR",  
        "errorDescription": "System.DmlException: Insert failed. First exception on row 0; first error: INVALID_EMAIL_ADDRESS, Email: invalid email address: a@213213213213213com: [Email]\n\nClass.LYB2B_PostLead.postLead: line 50, column 1"  
    }  
}
```

	Error Correo Ya Existe

```json
{  
    "error": {  
        "errorCode": 404,  
        "errorDateTime": "2024-03-21T11:33:09.429Z",  
        "errorMessage": "Not Acceptable",  
        "errorDescription": "Email waiting for finishing Sing-up process"  
    }  
}
```


Agent Form con Id y Email

```json
{
  "agency": {  
    "fiscalData": {  
      "status": "Pre",  
      "shippingAddress": {  
        "state": "Madrid",  
        "postalCode": "ES",  
        "country": "ES",  
        "city": "Madrid",  
        "address": null  
      },  
      "prefix": "+34",  
      "phone": "649765389",  
      "fiscalName": null,  
      "email": null,  
      "cif": null  
    },  
    "businessData": {  
      "webPage": "https://huakai.es/",  
      "shippingAddress": {  
        "state": "Madrid",  
        "postalCode": "28234",  
        "country": "ES",  
        "city": "Madrid",  
        "address": null  
      },  
      "idIATA": "ES22",  
      "businessName": "67TGF",  
      "agencyLoyaltyId": null  
    }  
  },
  "agentData": {
    "firstName": "Test",
    "lastName": "Test2",
    "email": "test@yopmail.com",
    "typeUser": "",
    "country": "AF",
    "memberReferalCode": "",
    "termsConds": "",
    "notifications": ""
  }
}

```

Sin Id

```json
{
    "agency": {
        "fiscalData": {
            "status": null,
            "shippingAddress": {
                "state": null,
                "postalCode": null,
                "country": null,
                "city": null,
                "address": null
            },
            "prefix": null,
            "phone": null,
            "fiscalName": null,
            "email": null,
            "cif": null
        },
        "businessData": {
            "webPage": null,
            "shippingAddress": {
                "state": null,
                "postalCode": null,
                "country": null,
                "city": null,
                "address": null
            },
            "idIATA": null,
            "businessName": null,
            "agencyLoyaltyId": null
        }
    },
    "agentData": {
        "firstName": "Test",
        "lastName": "Test2",
        "email": "test@yopmail.com",
        "typeUser": null,
        "country": "AF",
        "memberReferalCode": null,
        "termsConds": null,
        "notifications": null
    }
}
```


POST reviews-experience
```json
{

  "idReserve": "R23458",

  "overallExperience": 5,

  "titleOpinion": "Very relaxing",

  "description": "Very relaxing"

}
```

POST booking-manuals
```json
{
  "order": {
    "bookingType": "single",
    "voucherCode": "E456T",
    "bookingReference": "65434567B",
    "nameHotel": "BLESS",
    "startDate": "2024-09-21T00:00:00z",
    "endDate": "2024-09-21T00:00:00z",
    "numberRooms": 3,
    "groupName": "company",
    "promotionalCode": "34TG",
    "nameGuest": "Ana Piamonte"
  }
}

```

POST rewards-transferPoints
```json
{

  "pointsToRedeem": 50,
  "activityDate": "2024-09-21T00:00:00z",
  "isAuto": true,
  "isRedemptionToRewards": true

}
```