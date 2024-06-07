---
layout: page
---

# Change a shift property value

Update any property of a specific shift. Enter the ID number followed by the property name and value in the request body.

## HTTP method

PATCH

## URL

```shell
{server_url}/shifts/{id}
```

Sample request body.

```js
{
    "date": "2024-07-22",
    "status": "open"
}
```
