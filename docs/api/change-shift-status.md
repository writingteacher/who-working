layout: page
---

# Chanhge the status of a shift

Update the status of a shift. Set a shift to OPEN or CLOSED. Before updating a shift, the user must locate an existing shift by the ID.

## HTTP method

PATCH

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
| `id`     | Number | The unique ID assigned to the shift.  |
| `status`  | String | The shift is **Open** (waiting to fill the positon) or **Closed** (the positon is no longer available).|

## Example request body

```json
{
        "status": "closed"
}
```

```bash
curl --location --request PATCH 'http://localhost:3000/shifts/df91' \
--header 'Content-Type: application/json' \
--data '{
    "status": "closed"
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
    "status": "closed"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
