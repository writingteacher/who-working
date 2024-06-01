---
layout: page
---

# Quickstart guide

Busy managing a quickservice location?

Easily manage all your last-minute staffing requirements with one simple app!

## At a glance

This Quickstart provides all the information you need to begin using Who's Working to fill last minute staffing vacancies.

You’ll learn when and how to use the service and get set up to make your first call to the API.

## Setting up the Who's Working service

Shifts and Workers appear in the Who's Working service when they are created in the database.

You might need to set up your development system and get going from scratch. Don’t worry – you only have to do this one time per development system! Follow these [prerequisite steps](../tutorials/before-you-start-a-tutorial.md) to install the tools and test your development system.

## When to use the Who's Working service

The service REST API offers a wide range of integration possibilities, from enhancing internal workflow to creating customer-facing apps.

The service has two resources: [`shifts`](shifts) and [`workers`](workers). The [`shifts`](shifts) resource lists all restaurant shifts created in the database, including OPEN and CLOSED shifts. The [`workers`](workers) resource lists all trained workers who expressed an interest on working on an on-call basis for the quickservice location.

In Version 1, quickservice managers are responsible for managing shift and worker records. That includes creating, editing, and deleting records. Managers are also reponsible for pro-actively scanning the list of workers for possible matches. If they find a match, the manger contacts the worker via email or phone and continues the discussion off-app. In Version 2, workers who sign up for the service will have access to the app. They will be able to search for available shifts that align with their schedules and contact the shift manager.

## How to use the Who's Working service

To build your API call, you must have the following components:

* **A host.**  The {base_url} depends on users' installation of the service in their development environment. For v1 of the service API, the **base_url** variable is typically set to `http://localhost:3000`.
* **Authorization.**  For v1 of the service, requests do not use any authorization. All endpoints are available to all users and applications.
* **A request.**  The service REST API enables CRUD operations via HTTP requests on database resources (`GET`, `POST`, `PUT`, `PATCH`, and `DELETE` methods). Request and response bodies are encoded as JSON.

### Supported endpoints

#### Shifts

| :--------------: | :--------------: |
| HTTP Method | Endpoint |
| GET | [List all shifts](get-all-shifts.md) |
| GET | [List shifts by ID](get-shifts-by-id.md) |
| GET | [List shift by date](get-shift-by-date.md) |
| POST | [Create a shift](create-shift.md) |
| PUT | [Update shift by ID](update-shift-by-id.md) |
| PATCH | [Update shift properties](change-shift-property.md) |
| CREATE | [Create a shift](shift-create.md) |

#### Workers

| :--------------: | :--------------: |
| HTTP Method | Endpoint |
| GET | [List all workers](get-all-workers.md) |
| GET | [List workers by ID](get-workers-by-id.md) |
| GET | [List workers by email](users-get-user-by-email.md) |
| POST | [Create a worker](create-worker.md) |
| PUT | [Update worker by ID](update-worker-by-id.md) |
| PATCH | [Update worker email](change-user-email.md) |
| PATCH | [Update a worker property](update-worker-with-patch.md) |
| CREATE | [Create a worker](worker-create.md) |

## Make your first API call – *List all shifts*

Assume that you’re already enrolled in the Who's Working service and you want to list all shifts as a first call to the API.

Let’s test making this simple request to the [`shifts`](task) resource. You’ll use cURL to make the API call.

```bash

curl http://localhost:3000/shifts
```

If the call is successful, the response you receive will be a list of shifts from the Who's Working service such as you see in this example:

```js

  {
        "id": "1",
        "date": "2024-06-01",
        "start_time": "0700",
        "shift_length": "4",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "open"
  },
  {
        "id": "2",
        "date": "2024-06-03",
        "start_time": "1030",
        "shift_length": "4",
        "warning": "none",
        "location_detail": "Yorkville Mall",
        "status": "open"
  },
  {
        "id": "3",
        "date": "2024-06-04",
        "start_time": "1430",
        "shift_length": "4",
        "warning": "closing",
        "location_detail": "Yonge-Bloor",
        "status": "open"
  }

```

---

**NOTE:**
cURL comes installed by default on Mac operating systems. If you need to, install it from [here](https://curl.se/windows/).

---

## Next steps

Now that everything is set up correctly, you can take full advantage of the Who's Working service API! Go ahead and start posting new shifts or creating new workers. You’ll see how easy the API is to use.

If you need more guidance, the [Tutorials](../tutorials/before-you-start-a-tutorial.md) section of the API documentation walks through a common shift task. The finer details of the supported resources, endpoints and properties are in the API reference section. For more information, go [here](../index.md).
