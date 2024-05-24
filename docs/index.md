---
layout: page
---

# Who's Working API Documentation

Turn your app into a staffing solution

Who's Working is a cloud service that helps your shift managers find and fill staffing positions. It's an ideal tool for quick service operations that experience last minute staff shortages. The lightweight API provides access to list of trained part-time workers who might be available on short notice for a restautant shift.  data and functionality, allowing developers to build custom features and branded interfaces. The Who's Working API uses REST and returns HTTP response codes and responses encoded in JSON.

There are two resources.

**Workers** - Part time workers who sign up for the Who's Working service. The Workers resource includes endpoints to create, retrieve, update, and delete user information.

**Shifts** - Available shifts in the restaurant created by the shift manager. Each shift describes the day and time along hours and wanrings. The Shifts resource includes endpoints to create, retrieve, update, and delete shift records.


## Quickstart

[Quickstart (SineadC)](api/quickstart_sinead.md)

## Tutorials

Learn how to do common tasks within the Who's Working service. Do this tutorial to set up your development system for these tutorials. You only have to do this one time per development system.

* [Before you start a tutorial](tutorials/before-you-start-a-tutorial)

After your system is ready, these tutorials show you how to perform common tasks.

Shifts

* [Create a shift](x)
* [Edit a shift](x)
* [Delete a shift](x)
* [Add a new property to an existing shift](s)
* [Get a user by name](tutorials/get-a-user-by-name)
* [Get tasks by a property](tutorials/get-task-by-property.md)
* [Delete a worker](tutorials/delete-a-task)

Workers

* [Create a new worker](x)
* [Update a specific worker's information](x)
* [Add a new property to an existing worker](s)


## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service. When running a local test, the `{base_url}` is generally `http://localhost:3000`.

* [workers resource](api/workers)
* [shifts resource](api/shifts)
* [Endpoint index](api/endpoint-index)
* [Handling errors](api/handling-errors)
