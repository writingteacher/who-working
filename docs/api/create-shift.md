---
layout: page
---

# Create a shift

Create a new restaurant shift.

## HTTP method

POST

## URL

```shell
{server_url}/shifts
```

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `date`    | String | The date (YYYY-MM-DD) of the work shift. Use the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.|
| `start_time` | Integer | The shift's start time. Use 24 clock time with no colon.|
| `shift_length` | Decimal | The shift length measured in hours. Use numbers with one decimal place (e.g. 4.5).|
| `location_detail`  | String | A short description of the restaurant's location.|
| `status`  | String | The shift is **Open** (waiting to fill the positon) or **Closed** (the positon is no longer available).|

## Example request body

```json
{
        "date": "2024-07-21",
        "start_time": "0700",
        "shift_length": "6",
        "location_detail": "Eatons Centre",
        "status": "open"
}
```

```bash
curl --location 'http://localhost:3000/shifts' \
--header 'Content-Type: application/json' \
--data '{
        "date": "2024-07-21",
        "start_time": "0700",
        "shift_length": "6",
        "location_detail": "Eatons Centre",
        "status": "open"
}'
```

## Return body

```js
[
    {
    "id": "df91",
    "date": "2024-07-21",
    "start_time": "0700",
    "shift_length": "6",
    "warning": "opening",
    "location_detail": "Eatons Centre",
    "status": "open"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
