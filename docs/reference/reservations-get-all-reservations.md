# Reference: Get all reservations

## Method

```
GET
```

Gets a list of all reservations.

## URL

```
{{baseUrl}}/reservations
```


## Params

None

## Request headers

None

## Request body

None

## Sample Response

``` json
[
 [
    {
        "id": "B1001",
        "flightId": [
            "FL123"
        ],
        "passengerId": "P001",
        "seatNumber": "12A",
        "reservationStatus": "Confirmed",
        "purpose": "personal"
    },
    {
        "id": "B1002",
        "flightId": [
            "FL124"
        ],
        "passengerId": "P001",
        "seatNumber": "18B",
        "reservationStatus": "Confirmed",
        "purpose": "business"
    },
    {
        "id": "B1003",
        "flightId": [
            "FL125"
        ],
        "passengerId": "P002",
        "seatNumber": "22C",
        "reservationStatus": "Confirmed",
        "purpose": "business"
    },
    {
        "id": "B1005",
        "flightId": [
            "FL126"
        ],
        "passengerId": "P004",
        "seatNumber": "10A",
        "reservationStatus": "Confirmed",
        "purpose": "personal"
    },
    {
        "id": "B1004",
        "flightId": [
            "FL126"
        ],
        "passengerId": "P003",
        "seatNumber": "7D",
        "reservationStatus": "Cancelled",
        "purpose": "business"
    }
]  
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |