---
layout: page
---

# Update reservation by ID

 This resource updates a reservation at a time. 

## Prerequisites

1. The ```json-server``` is up and running.
1. You have installed the Postman Desktop application. 

If you need help with the prerequisites, refer to the [before-you-start-a-tutorial](before-you-start-a-tutorial.md) section.

## About this task

To update an existing [reservation](../reference/reservation.md) follow these steps: 

1. Open Postman.
1. Select **PATCH** method. 
1. Enter ```{{baseUrl}}/reservations/id```. Specify the ID for which you want to update
the existing properties: ```{{baseUrl}}/reservations/df6e```
1. In the **Body** tab, create ONLY the properties you want to modify for that 
reservation and submit your request.

Here's how a sample request may look like, you can :

```js
  {
    "purpose": "business",
    "reservationStatus": "Booked" 
}
 ```
 
Here's a sample response for the id = df6e.

```json
{
    "id": "df6e",
    "flightId": [
        "FL126"
    ],
    "passengerId": "P0031",
    "seatNumber": "10D",
    "purpose": "business",
    "reservationStatus": "Booked"
}
```

## Related information

- [Error handling](../reference/error-handling.md)

## Next step

- [Delete reservation](del-res.md)
