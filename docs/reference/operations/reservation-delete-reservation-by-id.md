# Delete reservation by ID

## Method

```
DELETE
```

Deletes a [reservation](../resource/reservation.md) resource specified by the `id` parameter, if it exists.

## URL

```shell
{{baseUrl}}/reservations/id
```

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The ID of a reservation that you want to delete. |

For example:

```shell
{{baseUrl}}/reservations/B1004
```

## Params

None

## Request headers

None

## Request body

None

## Return body

None

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Resource deleted successfully |
| 404 | Error | Specified task  not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
