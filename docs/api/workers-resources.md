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

The `workers` resource supports these operations.

### READ (GET)

* [Get all workers *endpoint*](get-all-workers.md)
* [Get workers by last name *endpoint*](get-worker-by-last-name.md)
* [Get workers by ID *endpoint*](get-worker-by-id)
* [Get workers by available days *complete*](get_workers_days.md)
* [Get workers by available time *endpoint*](get_workers_available_time.md)

### CREATE (POST)

* [Create a worker *complete*](create-worker.md)

### UPDATE (PUT/PATCH)

* [Change a worker property by ID *endpoint*](change-worker-property-by-id.md)

### DELETE

* [Delete a worker by ID *endpoint*](delete-worker-by-id.md)
