---
layout: page
---
# `shifts` resource

Base endpoint:

```shell
{server_url}/shifts
```

Contains information about the shifts saved to the Who's Working service. In Version 1, only registered store managers can create a shift.

## Resource properties

Sample `shifts` resource.

```js
{
    "id": "81a2",
    "date": "2024-06-11",
    "start_time": "0900",
    "shift_length": "6",
    "warning": "opening",
    "location_detail": "Eatons Centre",
    "status": "closed"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`     | number | The unique ID assigned to the shift.  |
| `date`    | string | The date (YYYY-MM-DD) of the work shift. Use the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.|
| `start_time` | integer | The shift's start time. Use 24 clock time with no colon.|
| `shift_length` | decimal | The shift length is measured in hours. Use numbers with one decimal place (e.g. 4.5).|
| `warning`     | number | The number of hours and minutes relative to the `date` to alert workers of the shift. This is normally a negative number to alert the user before the `date`. |
| `location_detail`  | string | A short description of the restaurant's location.|
| `status`  | string | The shift is **Open** (waiting to fill the position) or **Closed** (the position is no longer available).|

## Operations

The `shifts` resource supports these operations.

### READ (GET)

| Resource | Description |
| ------------- | ----------- |
| [Get shifts by status](get-shifts-by-status.md)  | Complete  |
| [Get all shifts](get-all-shifts.md)  | Endpoint  |
| [Get shift by ID](get-a-shift-by-id.md)           | Endpoint  |
| [Get shifts by date](get-shifts-by-date.md)       | Endpoint  |
| [Get shifts by shift length](get-shifts-by-length.md)            | Endpoint  |
| [Get shift by ID](get-a-shift-by-id.md)  | Endpoint  |
| [Get shifts by date](get-shifts-by-date.md)              | Endpoint  |
| [Get shifts by shift length](get-shifts-by-length.md)   | Endpoint  |

### CREATE (POST)

| Resource | Description |
| ------------- | ----------- |
| [Create a shift](create-shift.md)  | Complete  |

### UPDATE (PATCH)

| Resource | Description |
| ------------- | ----------- |
| [Change shift status](change-shift-status.md)  | Complete  |
| [Update shift property by ID](change-shift-by-id.md)  | Endpoint  |

### DELETE

| Resource | Description |
| ------------- | ----------- |
| [Delete a shift by ID](delete-shift-by-id.md)  | Complete  |
