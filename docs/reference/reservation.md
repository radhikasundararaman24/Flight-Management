---
layout: page
---

# `reservation` resource

Base endpoint:

```shell
{local_url}/reservations
```

Contains information about the users of the service.

To have a task in the service, the user must be added to the service first.

## Resource properties

Sample `reservations` resource

```js
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
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | string | Unique identifier of the reservation. |
| `flightId` | string | Unique identifier of the flight. |
| `passengerId` | string | The passenger's Id. |
| `seatNumber` | string | The passenger's seat information. |
| `reservationStatus` | string | The status of the booking. |
| `purpose` | string | Type of travel. |

## Operations

The `reservations` resource supports these operations.

### READ (GET)

* [Get all reservarions](reservations-get-all-reservations.md)


### CREATE (POST)

* [Create reservarions](reservations-create-reservation.md)

### UPDATE (PUT/PATCH)

* [Update travel type by reservation ID](reservations-update-by-id.md)
* [Change seat by reservation ID](reservations-change-seat.md)


### DELETE

* [Delete reservation by ID](reservation-delete-reservation-by-id.md)
