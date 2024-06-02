---
layout: page
---

# `passengers` resource

Base endpoint:

```shell
{base_url}/users
```

Contains information about the passengers of the service.

To have a reservation in the service, the passenger must be added to the service first.

## Resource properties

Sample `passenger` resource

```js
 {
    "id": "P004",
    "firstName": "Liu",
    "lastName": "Wei",
    "dob": "1978-12-01",
    "passportNumber": "D98765432",
    "nationality": "China"
  }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The passenger's id. |
| `firstName` | string | The passenger's first  name. |
| `lastName` | string | The passenger's last name. |
| `dob` | string | The passenger's date of birth. |
| `passportNumber` | number | The passenger's unique passport record number. |
| `nationality` | string | The passenger's nationality. |

## Operations

The `passengers` resource supports these operations.

### READ (GET)

* [Get all passengers](passengers-get-all-passengers.md)
* [Get all passengers by ID](passengers-get-passenger-by-id.md)
* [Get all passengers by name](passengers-get-passenger-by-name.md)


### CREATE (POST)

* [Create a passenger](passengers-create-passenger.md)

### UPDATE (PUT/PATCH)

* [Update email by passenger ID](passengers-update-by-id.md)


### DELETE

* [Delete passenger by ID](passengers-delete-passenger-by-id.md)