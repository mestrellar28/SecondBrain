
## get content-courses

https://anypoint.mulesoft.com/mocking/api/v1/links/1ae36069-aa2b-480c-8e0b-6389c0b70213/content/courses

```json
{
    "courses": [
        {
            "idCourse": "0123-ED",
            "name": "Curso Especial",
            "market": "Market del curso",
            "subMarket": "SubMarket del curso",
            "brand": "Brand del curso",
            "pointsGet": 70,
            "calification": "Calification del curso",
            "description": "Description Curso Especial",
            "expirationDate": "2025-09-30"
        }
    ]
}
```

## get transactions-lastMovements

https://anypoint.mulesoft.com/mocking/api/v1/links/1ae36069-aa2b-480c-8e0b-6389c0b70213/transactions/lastMovements/:loyaltyId?queryType=false


```json
{
    "movements": {
        "bookings": [
            {
			    "typeRoom": "Single",
			    "status": "Processed",
			    "reservationDate": "2024-04-28",
			    "points": 25,
			    "numberNights": 4,
			    "nameHotel": "Hotel Ibiza",
			    "idReserve": "R389823",
			    "dateCheckout": "2024-04-13T00:00:00.000Z",
			    "dateCheckin": "2024-04-12T00:00:00.000Z",
			    "customerName": "Roger Federer",
			    "commission": 0.01
			},
			{
			    "typeRoom": "Double",
			    "status": "Cancelled",
			    "reservationDate": "2024-06-28",
			    "points": 250,
			    "numberNights": 10,
			    "nameHotel": "Hotelito",
			    "idReserve": "R389824",
			    "dateCheckout": "2024-04-13T00:00:00.000Z",
			    "dateCheckin": "2024-04-12T00:00:00.000Z",
			    "customerName": "Pepito Perez",
			    "commission": 0.10
			},
			{
			    "typeRoom": "Double",
			    "status": "Pending",
			    "reservationDate": "2024-09-28",
			    "points": 25,
			    "numberNights": 6,
			    "nameHotel": "Hilton",
			    "idReserve": "R389825",
			    "dateCheckout": "2024-04-13T00:00:00.000Z",
			    "dateCheckin": "2024-04-12T00:00:00.000Z",
			    "customerName": "Corey Taylor",
			    "commission": 0.20
			},
        ],
        "points": [
			{
				"movementDate": "2024-07-28",
				"movementType": "Puntos",
				"detail": "Puntos por reserva",
				"numberPoints": 100,
				"status": "Pending",
				"economicValue": 230,
				"confirmationDate": '2024-07-28',
				"pointsDetail": {
					"pointType": "Basic",
					"nOfNights": 5,
					"hotelName": "TRS",
					"guestName": "Pepito Juarez",
					"expirationPointsDate": "2025-01-01",
					"campainName": "Bienvenida",
					"campaingDescription": "Campaña de bienvenida para nuevos agentes",
					"bookingReference": "R389823",
					"channel": "directo"
				}
			},
			{
				"movementDate": "2024-08-28",
				"movementType": "Reserva",
				"detail": "Puntos por reserva",
				"numberPoints": 100,
				"status": "Canceled",
				"economicValue": 230,
				"pointsDetail": {
					"pointType": "Basic",
					"nOfNights": 5,
					"hotelName": "TRS",
					"guestName": "Pepito Juarez",
					"expirationPointsDate": "2025-01-01",
					"campainName": "Bienvenida",
					"campaingDescription": "Campaña de bienvenida para nuevos agentes",
					"bookingReference": "R389823",
					"channel": "indirecto"
				}
			},
			{
				"movementDate": "2024-09-28",
				"movementType": "Caducidad",
				"detail": "Puntos por reserva",
				"numberPoints": 100,
				"status": "Procesed",
				"economicValue": 230,
				"pointsDetail": {
					"pointType": "Basic",
					"nOfNights": 5,
					"hotelName": "Bless",
					"guestName": "Pepito Juarez",
					"expirationPointsDate": "2025-01-01",
					"campainName": "Bienvenida",
					"campaingDescription": "Campaña de bienvenida para nuevos agentes",
					"bookingReference": "R389823",
					"channel": "indirecto"
				}
			},
			{
				"movementDate": "2024-10-28",
				"movementType": "Canje",
				"detail": "Puntos por reserva",
				"numberPoints": 100,
				"status": "Canceled",
				"economicValue": 230,
				"pointsDetail": {
					"pointType": "Basic",
					"nOfNights": 5,
					"hotelName": "Only You",
					"guestName": "Pepito Juarez",
					"expirationPointsDate": "2025-01-01",
					"campainName": "Bienvenida",
					"campaingDescription": "Campaña de bienvenida para nuevos agentes",
					"bookingReference": "R389823",
					"channel": "directo"
				}
			} 
		]
    },
    "filters": {
        "status": ["Pending", "Processed", "Booking", "CheckOut", "Cancelled"],
        "details": ["", "", ""],
        "nameHotel": ["Bless","Only You", "TRS"],
        "movementType": ["Reserva", "Puntos", "Caducidad", "Canje"],
        "totalOfRows": 100,
        "currentPageNumber": 1
    }
}
```

## get challenges-rankings

https://anypoint.mulesoft.com/mocking/api/v1/links/1ae36069-aa2b-480c-8e0b-6389c0b70213/content/challenges-rankings/:loyaltyId?forRankings=true

```json
{
    "challenges": [
        {
            "idChallenge": "0001-ES",
            "nameChallenge": "Viaje del año",
            "expirationDate": "2025-03-23",
            "description": "Viaje del año",
            "percentage": 40,
            "currentStep": 40,  
            "numberOfSteps": 40,
            "typerChallenge": 2,
            "iconId": ""
        }
    ],
    "rankings": [
        {
            "idRanking": "0001-TL",
            "nameRanking": "Cliente del año",
            "expirationDate": "2025-03-23",
            "description": "Cliente del año",
            "position": 5,
            "numberParticipants": 20,
            "score": 100,
            "typerChallenge": 1,
            "iconId": ""
        }
    ]
}
```

## get content-rankings-details

https://anypoint.mulesoft.com/mocking/api/v1/links/1ae36069-aa2b-480c-8e0b-6389c0b70213/content/rankings-details/:loyaltyId?idRanking=003-DF

```json
{
    "idRanking": "003-DF",
    "name": "Cliente del año",
    "expirationDate": "2025-04-28",
    "description": "Mejor cliente del año",
    "typeOfObjective": 80,
    "detail": "Detalles cliente del año",
    "remainingObjectiveAward": "Faltan 10 reservas para recibir el premio",
    
    "challengeData": {
        "percentage": "60%",
        "currentStep": 3,
        "numberOfSteps": 2
    },
    
    "rankingData": {
        "numberParticipants": 50,
        "scoreEarnable": 100,
        "firstPositionText": "500 reservas",
        "cutPositionText": "200 reservas",
        "currentPositionText": "50 reservas",
        "cutPositionNumber": 20,
        "currentPositionNumber": 15,
        "otherMemberRankings": [
            {
                "positionNumber": 14,
                "name": "Name Member Ranking",
                "country": "España",
                "pendingPoints": 60,
                "confirmedPoints": 150,
                "loyaltyId": '12818029'
            }
        ]
    }
}
```

## get Challenges And Rankings (Rankings Destacados Tipo AB)

```json
{
    "challenges": [
        {
            "idChallenge": "0001-ES",
            "nameChallenge": "Viaje del año",
            "expirationDate": "2025-03-23",
            "description": "Viaje del año",
            "percentage": 40,
            "currentStep": 2,
            "numberOfSteps": 5,
            "typerChallenge": 2
        }
    ],
    "rankings": [
        {
            "idRanking": "0001-TL",
            "nameRanking": "Cliente del año",
            "expirationDate": "2025-03-23",
            "description": "Cliente del año",
            "position": 5,
            "numberParticipants": 20,
            "score": 100,
            "remainingObjectiveAward": "Faltan 10 reservas para recibir el premio",
            "typeRanking": 1,
            "firstPositionText": "500 reservas",
            "cutPositionNumber": 10,
            "cutPositionText": "200 reservas",
            "currentPositionText": "50 reservas",
            "otherMemberRankings": [
            {
                "positionNumber": 10,
                "name": "Name Member Ranking",
                "country": "España",
                "pendingPoints": 30,
                "confirmedPoints": 250,
                "loyaltyId": '12818030'
            },
            {
                "positionNumber": 14,
                "name": "Name Member Ranking",
                "country": "España",
                "pendingPoints": 60,
                "confirmedPoints": 150,
                "loyaltyId": '12818029'
            }
        ]
        }
    ]
}
```
### primer item
Number: siempre es 1
Text: firstPositionText

### segundo item
Number: cutPositionNumber
Text: cutPositionText

### tercer item
Number: position
Text: currentPositionText

```json
[
    {
        "rankings": [
            {
                "typeRanking": 1,
                "score": 1,
                "remainingObjectiveAward": "TEST",
                "position": 15,
                "numberParticipants": 10,
                "nameRanking": "TEST",
                "idRanking": "TEST",
                "firstPositionText": "TEST",
                "expirationDate": "TEST",
                "description": "TEST",
                "cutPositionText": "TEST",
                "cutPositionNumber": 10,
                "currentPositionText": "TEST",
                "otherMemberRankings": [
                    {
                        "positionNumber": 1,
                        "name": "Pepito",
                        "loyaltyId": "TEST",
                        "confirmedPoints": 1000
                    }
                ],
            }
        ],
        "message": null,
        "errorCode": null,
        "challenges": [
            {
                "typeChallenge": 1,
                "percentage": 10,
                "numberOfSteps": 3,
                "nameChallenge": "TEST",
                "idChallenge": "TEST",
                "expirationDate": "TEST",
                "description": "TEST",
                "currentStep": 1
            }
        ]
    }
]
```

Saldo total

	totalPointsBalanceValue

Total aculado

	totalPointsAccumulated

Pending

	pendingPoints



http://localhost:4503/content/palladium-pro/es/inicio/login.html?challengeId=a0JVe000000NtrpMAC&rankingId=a0JVe000000O3G5MAK