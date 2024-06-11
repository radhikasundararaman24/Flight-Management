# Create reservation

---
layout: page
---

## METHOD

```shell
POST
```

Creates a new [`reservation`](reservation.md) for a passenger.
The request body contains the new reservation details. 

## URL

```shell

{{server_url}/reservations

```

## Request headers

No headers required.

## Request body

You must specify the required properties for the new reservation.  In the request body, specify a JSON representation of the [`reservation`](reservations.md) object. 
The following table lists the properties that are required when you create a reservation. 

| Property | Description | Type |
| -------------- | ------ | ------------ |
| passengerId | (**Required**) The unique identifier of the passenger to whom the reservation is assigned.| integer |
| seatNumber| (**Required**) Seat number | string |
| reservationStatus |(**Optional**) Indicates the status of your booking.| string | Required |  |
| purpose | (**Optional**) The due date of the task. | string |
|  flightId | (**Required**) Indicates the flight number. | string |



## Sample request

The POST body should look something like this. You can change the values of each property as you would like.

```js
[
  {
    "id": "B1004",
    "flightId": [
      "FL126"
    ],
    "passengerId": "P0026",
    "seatNumber": "10D",
    "reservationStatus": "Booked",
    "purpose": "personal"
  }
]
```

## Response body
The following example shows the response. *Note that the response
automatically creates and assigns an id = B1004 for each successful request.* 

```js
[
{
    "id": "B1004",
    "flightId": [
        "FL126"
    ],
    "passengerId": "P0026",
    "seatNumber": "10D",
    "reservationStatus": "Booked",
    "purpose": "personal"
}
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | Reservation data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
