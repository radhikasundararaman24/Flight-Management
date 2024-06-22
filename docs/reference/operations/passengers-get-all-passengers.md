# Get all passengers

## URL
```
{{baseUrl}}/passengers
```
Gets a list of all passengers.

## Params

None

## Request headers

None

## Request body

None

## Sample Response

``` json
[
    [
    {
        "email": "doejoe@abc.com",
        "id": "P001",
        "firstName": "John",
        "lastName": "Doe",
        "dob": "1985-10-10",
        "passportNumber": "A12345678",
        "nationality": "USA"
    },
    {
        "id": "P002",
        "firstName": "Jane",
        "lastName": "Smith",
        "dob": "1990-03-25",
        "passportNumber": "B87654321",
        "nationality": "Canada"
    },
    {
        "id": "P003",
        "firstName": "Carlos",
        "lastName": "Garcia",
        "dob": "1982-07-14",
        "passportNumber": "C23456789",
        "nationality": "Mexico"
    },
    {
        "id": "P004",
        "firstName": "Liu",
        "lastName": "Wei",
        "dob": "1978-12-01",
        "passportNumber": "D98765432",
        "nationality": "China"
    },
    {
        "id": "H4e1",
        "passengerId": "P0026",
        "firstName": "Ruba",
        "lastName": "Yuk",
        "dob": "1995-02-10",
        "passportNumber": "B129340238",
        "nationality": "Italy"
    }
]
]

```
## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |