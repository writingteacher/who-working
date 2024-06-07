---
layout: page
---

# Get workers by available days

Gets a list of workers filtered by their available day.

## HTTP method

GET

## URL

```shell
{server_url}/workers?available_days={value}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `available_days` | string | The worker's availability. The user enters one option: Weekdays, Weekends, or Both.|

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Example request body

```json
{
    "available_days":"weekdays"
}
```

```bash
curl --location --request GET 'http://localhost:3000/workers?available_days=weekdays' \
--header 'Content-Type: application/json' \
--data ' '
```

## Return body

```js
[
    {
        "id": "1",
        "last_name": "Smith",
        "first_name": "Ferdinand",
        "email": "f.smith@example.com",
        "phone": "416-555-1213",
        "available_days": "weekdays",
        "available_time": "all"
    },
    {
        "id": "4",
        "last_name": "Bailey",
        "first_name": "Bill",
        "email": "b.bailey@example.com",
        "phone": "416-555-1215",
        "available_days": "weekdays",
        "available_time": "mornings"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
