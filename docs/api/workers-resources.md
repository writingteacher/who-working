---
layout: page
---
# `workers` resource

Base endpoint:

```shell
{server_url}/workers
```

Contains information about the workers saved to the Who's Working service. In Version 1, only registered store managers can create a worker record. In Version 2, the roadmap includes a feature that will allow each registered worker to create and update their own record on the app.

## Resource properties

Sample `workers` resource.

```js
{
        "id": "1",
        "last_name": "Smith",
        "first_name": "Ferdinand",
        "email": "f.smith@example.com",
        "phone": "416-555-1213",
        "available_days": "weekdays"
        "available_time": "mornings"
}
```

| Property name | Type | Description | 
| ------------- | ----------- | ----------- | 
| `id`     | number | The unique ID assigned to the worker.|
| `last_name`    | string | The worker's family name. |
| `first_name`    | string | The worker's given name. |
| `email` | string | The worker's email address.|
| `phone` | string | The worker's phone number.|
| `available_days` | string | The worker's availability. The user enters one option: Weekdays, Weekends, or Both.|
| `available_time` | string | The worker's availability during the day. The user enters one or more options: Open, Mornings, Afternoons, Evenings, Close, or All.|

## Operations

The `workers` resource supports these operations. Resources with an **Endpoint** description provide the endpoint but do not have a full set of instructions.

### READ (GET)

| Resource | Description |
| ------------- | ----------- |
| [Get workers by available days](get_workers_days.md)  | Complete  |
| [Get all workers](get-all-workers.md)  | Endpoint  |
| [Get a worker by last name](get-worker-by-last-name.md)  | Endpoint  |
| [Get a worker by ID](get-worker-by-id)  | Endpoint  |
| [Get all workers by available time](get_workers_available_time.md)  | Endpoint  |

### CREATE (POST)

| Resource | Description |
| ------------- | ----------- |
| [Create a worker](create-worker.md)  | Complete  |

### UPDATE (PATCH)

| Resource | Description |
| ------------- | ----------- |
| [Change a worker property by ID](change-worker-property-by-id.md)  | Endpoint  |

### DELETE

| Resource | Description |
| ------------- | ----------- |
| [Delete a worker by ID](delete-worker-by-id.md)  | Endpoint  |
