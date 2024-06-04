---
layout: page
---


# Show all reservations

 This resource retrieves all the reservations in the source. 

## Prerequisites

1. The ```json-server``` is up and running.
1. You have installed Postman Desktop. 
1. The Postman request collection setup is complete. 


## About this task

To show all reservations by ID:


1. Open Postman. 
1. In **Workspaces** > click **Import**.
1. Browse to the path containing the import collection and select the import file you want to test. For example: *flight-mgmt-API.postman_collection*.
1. From the top right corner, select the appropriate environment from the drop-down list. If you haven't set the environment, see [set up base URL](set-up-env-postman).
1. From the left pane, expand the imported API  collection.
1. Select the **GET** all reservations request.
1. Click **Send**.

Here's a sample of all reservations:

```js
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
        "passengerId": "P003",
        "seatNumber": "7D",
        "reservationStatus": "Cancelled",
        "purpose": "business"
    }
]
```


