---
layout: page
---
# `workers` resource

Base endpoint:

```shell
{server_url}/workers
```

Contains information about the workers saved to the Who's Working service. In Version 1, only registered store managers can create a worker record. In Version 2, the roadmap includes a feature that will allow registered workers to their own record on the app.

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
| `id`     | Number | The unique ID assigned to the worker.|
| `last_name`    | String | The worker's family name. |
| `first_name`    | String | The worker's given name. |
| `email` | String | The worker's email address.|
| `phone` | String | The worker's phone number.|
| `available_days` | String | The worker's availability. The user enters one option: Weekdays, Weekends, or Both.|
| `available_time` | String | The worker's availability during the day. The user enters one or more options: Open, Mornings, Afternoons, Evenings, Close, or All.|

## Operations

The `workers` resource supports these operations.

### READ (GET)

* [Get all workers](workers-get-all-workers)
* [Get workers by last name](workers-get-workers-by-last-name)
* Get workers by ID
* Get workers by available_days
* Get workers by available time


### CREATE (POST)

* [Create a worker](workers-create-worker)

### UPDATE (PUT/PATCH)

* [Change a worker email](workers-change-worker-email)
* Update worker by ID
* Change workers available_time

### DELETE

* [Delete a worker by ID](workers-delete-worker-by-id)
