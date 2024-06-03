---
layout: page
---

# Tutorial: Find a specific shift and update two properties

In this tutorial, you learn how to find a shift and update properties with the `PATCH` METHOD. The use case is very practical - a store manager creates a new shift by locating an old one with a **CLOSED** status and then changing the shift date and status (from CLOSED to OPEN). Knowing how to update a shift helps store managers save time. They can quickly generate anew  shift from a previous record and avoid creating a new shift from scratch.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Locating an existing shift

The first step is to display a list of shifts with the CLOSED status, find the record that needs to be updated, and note the ID number. Viewing a specific shift record requires the `GET` method.

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{server_url}/shifts?status=closed`
    * **Headers**:`Content-Type: application/json`
    * **Request body**: None

Sample call for shift ID 81a2.
```bash
curl --location 'http://localhost:3000/shifts?id=81a2'
```

In the Postman app, select **Send** to make the request. The service returns a JSON object that contains all closed shifts. Each shift has the following format. Note the `id` of the shift to update.

```js
{
    "id": "03b6",
    "date": "2024-06-11",
    "start_time": "0900",
    "shift_length": "6",
    "warning": "opening",
    "location_detail": "Eatons Centre",
    "status": "closed"
},
{
    "id": "03d3",
    "date": "2024-06-11",
    "start_time": "0900",
    "shift_length": "6",
    "warning": "opening",
    "location_detail": "Eatons Centre",
    "status": "closed"
} 
```

## Updating shift information

Now that you know the shift `id`, send a PATCH request to the /shifts/{id} endpoint to update the record.

To update the task description:

In Postman, create a new request with these values:

* **METHOD**: PATCH
* **URL**: `{server_url}/shifts/{id}`
* **Headers**:`Content-Type: application/json`
* **Request body**: None

Sample call for shift ID 81a2.
```bash
curl --location --request PATCH 'http://localhost:3000/shifts/81a2' \
--header 'Content-Type: application/json' \
--data '{
    "date": "2024-07-13",
    "status": "open"
}'
```

In the Request Body, add the properties and parameters that require an update. In this example, the date changes to July 13, and the status changes from `OPEN` to `CLOSED`.

```js
{
    "date": "2024-07-13",
    "status": "open"
}
```

Click **Send**. The service updates the shift record and returns a 200 OK along with the updated task as a JSON object.

```js
{
    "id": "03b6",
    "date": "2024-07-13",
    "start_time": "0900",
    "shift_length": "6",
    "warning": "opening",
    "location_detail": "Eatons Centre",
    "status": "open"
}
 ```

## Next Steps

Now that you have verified this API workflow in Postman, you’re ready to integrate it into your application. For more information, contact your customer success manager or read our
 [Quickstart guide](../api/quickstart_working.md)

## Related Topics

* [Shifts resources](docs/api/shifts-resources.md)
* [Workers resources](docs/api/workers-resources.md)
