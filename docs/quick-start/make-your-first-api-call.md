---
layout: page
---

# Make your first API call

 Let us try adding a new reservation to the Flight Management database.

## Prerequisites

1. The ```json-server``` is up and running.
1. You have installed the Postman Desktop application.
1. The Postman request collection setup is complete.

If you need help with the prerequisites, refer to the [before-you-start-a-tutorial](before-you-start-a-tutorial.md) section.

## About this task

To add a new [reservation](../reference/resource/reservation.md) follow these steps:

1. Open Postman.
1. Select **POST** method.
1. Enter ```{{baseUrl}}/reservations```.
1. In the Body tab, create the following properties for a new reservation and submit your request:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | string | (**Required**) Unique identifier of the reservation. |
| `flightId` | string | (**Required**) Unique identifier of the flight. |
| `passengerId` | string | (**Required**) The passenger's Id. |
| `seatNumber` | string | (**Required**) The passenger's seat information. |
| `reservationStatus` | string | (**Optional**) The status of the booking. |
| `purpose` | string | (**Optional**) Type of travel. |

Here's how a sample request may look like, you can :

```js
  {
    
    "flightId": [
      "FL126"
    ],
    "passengerId": "P0031",
    "seatNumber": "10D"
   
    
  }
 ```

 Here's a sample response: of all reservations:

```json
{
    "id": "df6e",
    "flightId": [
        "FL126"
    ],
    "passengerId": "P0031",
    "seatNumber": "10D"
}
```

**NOTE**: The response automatically generates an "id" for each new reservation.
This id is unique and associated with the passenger's information.

## Next step

- [Get started with our tutorials](../tutorials/all-tutorials.md)

## Related information

- [Error handling](../reference/error-handling.md)