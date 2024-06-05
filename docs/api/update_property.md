---
layout: page
---

# Update a shift with PATCH

Use `PATCH` to update a shift and update some of the information in a record. To update a specific shift, you must supply the task `id` in both the request endpoint and request body.

## Endpoint

The endpoint for using `PATCH` to update a task is:

```
{server_url}/shifts/{id}
```

## Properties

The following example contains a request body for a `PATCH` request.

```json
{
        "id": "03b6",
        "date": "2024-06-11",
        "start_time": "0900",
        "shift_length": "6",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "closed"
}
```

## Descriptions

The following table defines properties in the request body.

| Property name | Type   | Description                                                                                                                                                 |
| ------------- | ------ | ------------------------- |
| `id`     | number | The unique ID assigned to the shift. record.  |
| `date`    | string | The date (YYYY-MM-DD) of the work shift. Use the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.|
| `start_time` | integer | The shift's start time. Use 24 clock time with no colon.|
| `shift_length` | string | The shift length measured in hours. Use integers with one decimal place (e.g. 5.5).|
| `warning`     | number | The number of hours relative to the `date` to alert the workers of the shift. This is normally a negative number to alert the user before the `date`. |
| `location_detail`  | string | A short description of the restaurant's location.|
| `status`  | string | The available shift is **Open** (waiting to fill the positon) or **Closed** (the positon is no longer available).|

## Operations

When you use `PATCH` to update a task, you can:

* **Update an entire task** — Replace the entire request body.
* **Update part of a task** — Only replace the fields to update; omit the others. 

> ℹ️ Task `id` is required in both scenarios and must match in both the endpoint and the request body. For example, if you change the `id` in only the request body, the service returns a `200 OK`, but does not update the task. 

## Examples

Use the following examples when sending `PATCH` requests to the To-Do service.

### cURL

```bash
curl --location --request PATCH '{server_url}:{port}/tasks/4' \
--header 'Content-Type: application/json' \
--data '{
  "user_id": 3,
  "title": "Title of my task",
  "description": "Name of my task",
  "due_date": "2024-05-15T14:00",
  "warning": "-20",
  "id": 4
}'
```

### Complete task body

```json
{
  "user_id": 3,
  "title": "Get shots for my cat", 
  "description": "Annual vaccinations for Sophie", 
  "due_date": "2024-05-15T14:00", 
  "warning": "-20",
  "id": 4
}
```
### Partial task body

```json
{
  "description": "Annual vaccinations for Zeke",
  "id": 4
}
```
## Related topics

- [Task resource](task.md)
- [Handling errors](handling-errors.md)