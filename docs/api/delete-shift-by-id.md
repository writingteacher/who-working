---
layout: page
---

# Delete a shift

Permanently remove a restaurant shift from the service. Before deleting a shift, the user must locate an existing shift by the ID.

## HTTP method

DELETE

## URL

```shell
{server_url}/shifts/{id}
```

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`     | number | The unique ID assigned to the shift.  |

## Example request body

```json
[
        {
        "date": "2024-08-11",
        "start_time": "0700",
        "shift_length": "6.5",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "open"
        }
]
```

```

```bash
curl --location --request DELETE 'http://localhost:3000/shifts/5a9b' \
--header 'Content-Type: application/json' \
--data '{
        "date": "2024-08-11",
        "start_time": "0700",
        "shift_length": "6.5",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "open"
}'
```

## Return body

```js
{
    "id": "5a9b",
    "date": "2024-08-11",
    "start_time": "0700",
    "shift_length": "6.5",
    "warning": "opening",
    "location_detail": "Eatons Centre",
    "status": "open"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
