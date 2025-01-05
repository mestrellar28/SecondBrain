
### Rewards Exchange Module

success
```json
{
  "message": {
    "code": 201,
    "dateTime": "2024-05-01T11:19:41.667Z",
    "description": "successful transaction"
  }
}
```

error
```json
{
  "error": {
    "errorCode": 409,
    "errorDateTime": "2024-05-01T11:21:15.263Z",
    "errorMessage": "Not enough points to transfer",
    "errorDescription": "Not enough points to transfer"
  }
}
```

error
```json
{
    "error": {
        "errorCode": 500,
        "errorDateTime": "2024-05-01T11:21:52.413Z",
        "errorMessage": "System.DmlException: Insert failed. First exception on row 0; first error: FIELD_INTEGRITY_EXCEPTION, Select a loyalty program member.: []\n\nClass.LYB2B_PointsRedemption.insertTransactionRedemption: line 277, column 1\nClass.LYB2B_PostTransferPoints.postTransferPoints: line 38, column 1",
        "errorDescription": "System.DmlException: Insert failed. First exception on row 0; first error: FIELD_INTEGRITY_EXCEPTION, Select a loyalty program member.: []\n\nClass.LYB2B_PointsRedemption.insertTransactionRedemption: line 277, column 1\nClass.LYB2B_PostTransferPoints.postTransferPoints: line 38, column 1"
    }
}
```


### Form Review

success
```json
{
    "message": {
        "code": 201,
        "dateTime": "2024-05-02T07:25:25.488Z",
        "description": "successful transaction"
    }
}
```


### Form Manual Reservation

error
```json
{
    "errorCode": 400,
    "errorDateTime": "2024-05-02T07:58:14",
    "errorMessage": "HTTP POST on resource 'https://s-palladium-pro-loyalty-api-uat.de-c1.cloudhub.io:443/agent-loyalty-adobe/api/v1/booking/manuals/2404066439' failed: bad request (400).",
    "errorDescription": "Bad request. HTTP POST on resource 'https://s-palladium-pro-loyalty-api-uat.de-c1.cloudhub.io:443/agent-loyalty-adobe/api/v1/booking/manuals/2404066439' failed: bad request (400)."
}
```


### Agency Form

error
```json
{
    "errorCode": 404,
    "errorDateTime": "2024-05-02T10:03:34.187Z",
    "errorMessage": "Member Lead was not found in the system",
    "errorDescription": "Member Lead was not found in the system"
}
```
