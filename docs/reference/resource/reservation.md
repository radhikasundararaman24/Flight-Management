---
layout: page
---

# `Reservation` resource

Base endpoint:

```shell
{local_url}/reservations
```

Contains information about the users of the service.

To have a task in the service, the user must be added to the service first.

## Reservation properties

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
| `id` | string | (**Required**) Unique identifier of the reservation. |
| `flightId` | string | (**Required**) Unique identifier of the flight. |
| `passengerId` | string | (**Required**) The passenger's Id. |
| `seatNumber` | string | (**Required**) The passenger's seat information. |
| `reservationStatus` | string | (**Optional**) The status of the booking. |
| `purpose` | string | (**Optional**) Type of travel. |

## Operations

The `reservations` resource supports these operations.

### READ (GET)

* [Get all reservarions](../operations/reservations-get-all-reservations.md)


### CREATE (POST)

* [Create reservarions](../operations/reservations-create-reservation.md)

### UPDATE (PUT/PATCH)

* [Update travel type by reservation ID](../operations/reservations-update-by-id.md)

### DELETE

* [Delete reservation by ID](../operations/reservation-delete-reservation-by-id.md)
