---
layout: page
---

# Delete reservation by ID

 This resource updates a reservation at a time.

## Prerequisites

1. The ```json-server``` is up and running.
1. You have installed the Postman Desktop application.

If you need help with the prerequisites, refer to the [before-you-start-a-tutorial](../quick-start/before-you-start-a-tutorial.md) section.

## About this task

To update an existing [reservation](../reference/resource/reservation.md) follow these steps:

1. Open Postman.
1. Select **DELETE** method.
1. Enter ```{{baseUrl}}/reservations/id```. Specify the ID of
the existing reservation that you want to delete: ```{{baseUrl}}/reservations/df6e```
1. Click **Send**.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related information

- [Error handling](../reference/error-handling.md)