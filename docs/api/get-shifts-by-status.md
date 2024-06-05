---
layout: page
---

# Get shifts by status

Gets a list of shifts filtered by their `OPEN` or `CLOSED` status.

## HTTP method

GET

## URL

```shell
{server_url}/shifts?status={value}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `status` | string | The status of the shift. The status options are OPEN or CLOSED. |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `status` | string | Open or closed.  |

## Example request body

```json
{
    "status": "closed"
}
```

```bash
curl --location --request GET 'http://localhost:3000/shifts?status=closed' \
--header 'Content-Type: application/json' \
--data '{
    "status": "closed"
}'
```

## Return body

```js
[
    {
        "id": "03b6",
        "date": "2024-07-13",
        "start_time": "0900",
        "shift_length": "6",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "closed"
    },
    {
        "id": "03d3",
        "date": "2024-06-11",
        "start_time": "0900",
        "shift_length": "6",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "closed"
    },
    {
        "id": "81a2",
        "date": "2024-06-11",
        "start_time": "0900",
        "shift_length": "6",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "closed"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
