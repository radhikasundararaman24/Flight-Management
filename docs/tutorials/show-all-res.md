---
layout: page
---


# Show all reservations

 This resource retrieves all the reservations in the source. 

## Prerequisites

1. The ```json-server``` is up and running.
1. You have installed the Postman Desktop application. 

If you need help with the prerequisites, refer to the [before-you-start-a-tutorial](before-you-start-a-tutorial.md) section.

## About this task

To show all reservations:

1. Open Postman. 
1. Select the **GET** method.
1. Enter ```{{baseUrl}}/reservations```.
1. Click **Send**.

Here's a sample of all reservations:

```js
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
```

## Related information

- [Error handling](../reference/error-handling.md)

## Next step

- [Update reservation](update-reservation.md)



