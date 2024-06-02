---
layout: page
---

# `flights` resource

Base endpoint:

```shell
{local_url}/flights
```

Contains information about the flights of the service.


## Resource properties

Sample `flights` resource

```js
 {
    "id": "FL126",
    "flightNumber": "OA321",
    "airline": "Oceanic Airlines",
    "origin": "MIA",
    "destination": "JFK",
    "departureTime": "2024-06-02T12:00:00Z",
    "arrivalTime": "2024-06-02T15:00:00Z"
  }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The flight's id. |
| `flightNumber` | string | The flight's number. |
| `airline` | string | The airline name. |
| `origin` | string | The starting location of the airline. |
| `destination` | string | The final destination of the airline. |
| `departureTime` | dateTime | Time of departure. |
| `arrivalTime` | dateTime | Time of arrival. |

