# Update reservation by ID

---
layout: page
---

## Method

```
PATCH
```

The Patch request updates the reservation's travel type but does not change the other parameters in the [`reservation`](../resource/reservation.md) object.

**Note** : *After creating a reservation, a unique identifier (ID) is assigned. Provide the ID for the reservation in the base URL.*

## URL

```shell
{server_url}/reservations/{id}
```

In the URL, specify the ID of the reservation that you want to modify. To find the reservation
id, do a [get all reservations](../operations/reservations-get-all-reservations.md).

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | (**Required**) The reservations's unique record ID. |

For example:

```shell
{server_url}/reservations/{df6e}
```

## Params

None

## Request headers

None

## Request body

To add a travel type or update the status of your booking for an existing reservation, you can have the following in the
request.

```shell
{
    "purpose": "business",
    "reservationStatus": "Booked" 
}
```

## Return body

The following response shows a successful update for the reservation ID = df6e.

```
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

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Removes the user and returns an empty response. |
| 404 | Error | Specified user record not found. |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |