---
layout: page
---

# Change a worker property value

Update any property of a specific worker record. Enter the ID number followed by the property name and value in the request body.

## HTTP method

PATCH

## URL

```shell
{server_url}/workers/{id}
```

Sample request body.

```js
{
    "available_days": "weekdays",
    "available_time": "open"
}
```