# About the Flight Management API

The Flight Management API service provides a comprehensive solution
for managing flights, passengers, and reservations efficiently.
With this API, users can seamlessly access and manipulate data
related to flights, passengers, and their reservations.

## How does this API service work?

Here’s a "Hello World" example to demonstrate how the Flight Management API service works.

**Scenario**: Let's say you want to retrieve a list of all flights using the Flight Management API.

**HTTP Method**: GET

Our Flight Management API uses *HTTP Methods* for handling requests and responses.
The **HTTP GET** method works by sending a request to the Flight Management API, which then retrieves and returns
a list of flights. You can specify parameters such as date,
destination, and airline to filter the results.

## Technical Specifications

The Flight Management API needs the following components to operate.

- [Node.js v20.14.0](https://nodejs.org/en/download/package-manager)
- [Json-server 1.0.0-beta.1](https://www.npmjs.com/package/json-server)
- [CURL](https://curl.se/download.html)

**Note**: The devlopment system instructions are tested on *Windows* operating system.

To explore further, take a look at the [First Steps](../quick-start/before-you-start-a-tutorial.md).  

## API Security

There is no authentication and authorization. You can try our API endpoints "*as is*".

## Quick test

Are you a seasoned developer? You can jump right in and test this API using these steps.

**This task can take up to 10 minutes**.  

Follow these steps for testing your first call in *Windows* development system:  

1. **Install components**: Download and install the technical specifications.
1. **Access the API endpoints**: Fork the [repo](https://github.com/radhikasundararaman24/flight-management-service).
1. **Start server**: Go to command-line prompt and start the json-server:

    ```shell
      cd <your GitHub repo workspace>
      cd flight-management-service
      cd api
      cd start-server.bat
    ```

1. **Make your first API call**: Open another command-line window and submit the following request to retrieve a list of flights.

    **Sample request:**

    ```curl
    http://localhost:3000/reservations
    ```

    **Sample response:**

    ```json
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
    ```

## Supported endpoints

This version supports the following endpoints and operations:

| Method | Operation  |
|---|---|
| GET  | [Retrieve all reservations](../reference/operations/reservations-get-all-reservations.md). |
| CREATE  | [Add reservation](../reference/operations/reservations-create-reservation.md). |
| GET  | [Retrieve all passengers](../reference/operations/passengers-get-all-passengers.md). |
| PATCH  | [Modify the existing reservation record by ID](../reference/operations/reservations-update-by-id.md). |
| DELETE  | [Delete reservation by id](../reference/operations/reservation-delete-reservation-by-id.md). |

## Related information

- [Tutorials](../tutorials/all-tutorials.md)