---
layout: page
---

# Overview

The Flight Management API service provides a comprehensive solution
for managing flights, passengers, and reservations efficiently.
With this API, users can seamlessly access and manipulate data
related to flights, passengers, and their reservations.

![image_flight-mgmt.svg](image_flight-mgmt.svg)

## API Security

The API uses Basic Auth authentication which validates the following
information in the HTTP Authorization header: 
- username 
- password  

The credentials are encoded in Base64Links to an external site. 
For more resources on Basic Auth, visit: [security in Swagger](https://swagger.io/docs/specification/2-0/authentication/basic-authentication/).

## Quick start

Here’s a "Hello World" example to demonstrate how the Flight Management API service works.

**Scenario**

Let's say you want to retrieve a list of all flights using the Flight Management API.

### Steps

1. Set up the environment: Ensure you have access to the API endpoint and the necessary API key for authentication.
1. Create or import a Postman collection: If you're using Postman, you can create a new collection or import one that contains predefined API requests.
1. Set up the Base URL.
1. Make your first API call: Use the API endpoint from the collection to retrieve a list of flights.

**Sample request:** 

``` curl
curl http://localhost:3000/reservations
```

**Sample response:**

```json
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
    "passengerId": "P0031",
    "seatNumber": "10D"
  }
]
```

## Supported endpoints

The following table shows the list of operations offered by this service:


| Method | Operation  | 
|---|---|
| GET  | [Retrieve all reservations](reference/reservations-get-all-reservations.md). |
| GET  | [Retrieve all passengers](reference/passengers-get-all-passengers.md). |
| PATCH  | [Modify the existing reservation record by ID](reference/reservations-update-by-id.md). |
| DELETE  | [Delete reservation by id](reference/reservation-delete-reservation-by-id). | 


## Related information

- [Quick start](tutorials/before-you-start-a-tutorial.md)
- [Supported endpoints](reference/endpoints.md)

