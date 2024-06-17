---
layout: page
---

# All about the Flight Management API

The Flight Management API service provides a comprehensive solution
for managing flights, passengers, and reservations efficiently.
With this API, users can seamlessly access and manipulate data
related to flights, passengers, and their reservations.

## Technical Specifications for trying this service 

In a nutshell, the Flight Management API needs the following components to operate:

    - Node.js v20.14.0 
    - Json-server 1.0.0-beta.1
    - CURL version: 8.8.0 

To explore further, take a look at the [First Steps](tutorials/before-you-start-a-tutorial.md).  

## API Security

The API uses Basic Auth authentication which validates the following
information in the HTTP Authorization header: 

    - username 
    - password  

The credentials are encoded in Base64Links to an external site. 
For more resources on Basic Auth, visit: [security in Swagger](https://swagger.io/docs/specification/2-0/authentication/basic-authentication/).

## How does this service work?

Here’s a "Hello World" example to demonstrate how the Flight Management API service works.

**Scenario**

Let's say you want to retrieve a list of all flights using the Flight Management API.

Our Flight Management API uses *HTTP Methods* for handling requests and responses. 
The **HTTP GET** method works by sending a request to the Flight Management API, which then retrieves and returns
a list of flights. You can specify parameters such as date, 
destination, and airline to filter the results.

### Quick start

1. **Install components**: Download and install the technical specifications. 
1. **Authenticate**: Set up the necessary API security keys.
1. **Access the API endpoints**: Fork the [repo](https://github.com/radhikasundararaman24/flight-management-service).
1. **Start server**: Go to command-line prompt and start the json-server:
        
    ```shell
    cd <your GitHub repo workspace>
    # (see the flight-management-service directory in the list)
    cd flight-management-service
    cd api
    cd start-server.bat
    ```     
1. **Make your first API call**: Open another command-line window and submit the following request to retrieve a list of flights.

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

This version supports the following endpoints and operations:


| Method | Operation  | 
|---|---|
| GET  | [Retrieve all reservations](reference/reservations-get-all-reservations.md). |
| CREATE  | [Add reservation](reference/reservations-create-reservation.md). |
| GET  | [Retrieve all passengers](reference/passengers-get-all-passengers.md). |
| PATCH  | [Modify the existing reservation record by ID](reference/reservations-update-by-id.md). |
| DELETE  | [Delete reservation by id](reference/reservation-delete-reservation-by-id). | 


## Related information

- [Quick start](tutorials/before-you-start-a-tutorial.md)
- [Tutorials](tutorials/usecase.md)

