---
layout: page
---

# Create a worker

Create a restaurant worker record.

## HTTP method

POST

## URL

```shell
{server_url}/workers
```

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body parameters

| Property name | Type | Description | 
| ------------- | ----------- | ----------- | 
| `last_name`    | string | The worker's family name. |
| `first_name`    | string | The worker's given name. |
| `email` | string | The worker's email address.|
| `phone` | string | The worker's phone number.|
| `available_days` | string | The worker's availability. The user enters one option: Weekdays, Weekends, or Both.|
| `available_time` | string | The worker's availability during the day. The user enters one or more options: Open, Mornings, Afternoons, Evenings, Close, or All.|

## Example request body

```json
{
        "last_name": "Green",
        "first_name": "Jackie",
        "email": "green@example.com",
        "phone": "010-1212-1212",
        "available_days": "both",
        "available_time": "all"
}
```

```bash
curl --location 'http://localhost:3000/workers' \
--header 'Content-Type: application/json' \
--data-raw ' {
"last_name": "Green",
"first_name": "Jackie",
"email": "green@example.com",
"phone": "010-1212-1212",
"available_days": "both",
"available_time": "all"
 }'
```

## Return body

```js
{
    "id": "c08e",
    "last_name": "Green",
    "first_name": "Jackie",
    "email": "green@example.com",
    "phone": "010-1212-1212",
    "available_days": "both",
    "available_time": "all"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
