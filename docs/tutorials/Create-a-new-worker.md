---
layout: page
---

# Tutorial: Create a new worker

In this tutorial, you learn how to create a new worker record with the `POST` METHOD. The use case is very practical. In Version 1 of the service, each store manager must create worker records. In Version 2, store employees who sign up for the service will be able to create their own app records.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start](before-you-start-a-tutorial) checklist on the development system you'll use for the tutorial.

## Creating a record

To create a worker record:

Go to Postman and create a new request with these values:

* **METHOD**: POST
* **URL**: `{server_url}/workers`
* **Headers**:`Content-Type: application/json`

Sample call for shift ID 03b6.
```bash
curl --location 'http://localhost:3000/workers' \
--header 'Content-Type: application/json' \
--data-raw '    {
        "last_name": "Jones",
        "first_name": "Barry",
        "email": "bjones@yopmail.com",
        "phone": "905-555-2222",
        "available_days": "weekdays",
        "available_time": "all"
    }'
```

In the Request Body, add the properties and parameters that require an update. In this example, the date changes to July 22, and the status changes from `CLOSED` to `OPEN`.

```js
{
        "last_name": "Jones",
        "first_name": "Barry",
        "email": "bjones@yopmail.com",
        "phone": "905-555-2222",
        "available_days": "weekdays",
        "available_time": "all"
}
```

Click **Send**. The service creates a new worker record and returns a 200 OK along with the updated task as a JSON object.

```js
{
    "id": "f61b",
    "last_name": "Jones",
    "first_name": "Barry",
    "email": "bjones@yopmail.com",
    "phone": "905-555-2222",
    "available_days": "weekdays",
    "available_time": "all"
}
 ```

## Next Steps

Now that you have verified this API workflow in Postman, you’re ready to integrate it into your application. For more information, contact your customer success manager or read our
 [Quickstart guide](../api/quickstart_working.md)

## Related Topics

* [Shifts resources](../api/shifts-resources.md)
* [Workers resources](../api/workers-resources.md)