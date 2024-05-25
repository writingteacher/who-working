---
layout: page
---

# Who's Working API Documentation

Turn your app into a staffing solution

Who's Working is a cloud service that helps your shift managers find trained part-time workers and fill staffing positions. It's an ideal tool for quick service operations that experience last minute staff changes. The lightweight API provides access to a list of trained part-time workers who might be available on short notice for a restaurant shift. The Who's Working API uses REST and returns HTTP response codes and responses encoded in JSON.

There are two resources.

**Workers** - Part time workers who sign up for the Who's Working service. The Workers resource includes endpoints to create, retrieve, update, and delete user information.

**Shifts** - Available shifts in the restaurant created by the shift manager. Each shift describes the location, day and time along hours, and warnings. The Shifts resource includes endpoints to create, retrieve, update, and delete shift records.

## Quickstart

[Quickstart](x)

## Tutorials

Learn how to do common tasks within the Who's Working service. Do this tutorial to set up your development system. Complete the set up one time per development system.

* [Before you start a tutorial](x)

After your system is ready, select a tutorial and learn how to perform common tasks.

Shifts

* [Create a shift](tutorials/x)
* [Edit a shift](tutorials/x)
* [Delete a shift](tutorials/x)
* [Copy a shift and change a property](tutorials/x)
* [Add a new property to an existing shift](s)
* [Get a worker by a property](tutorials/x)

Workers

* [Create a new worker](x)
* [Update a specific worker's information](x)
* [Add a new property to an existing worker](x)
* [Delete a worker](tutorials/x)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service. When running a local test, the `{base_url}` is generally `http://localhost:3000`.

[Workers resource api/workers](api/workers)

READ (GET)

* Get all workers
* Get worker by availability
* Get worker by property

CREATE (POST)

* Create worker

UPDATE (PUT/PATCH)

* Change worker email
* Change worker property

DELETE

* Delete worker by ID

[Shifts resource api/shifts](api/shifts)

READ (GET)

* Get all shifts
* Get shift by status
* Get shift by property

CREATE (POST)

* Create a shift

COPY (COPY)

* Copy a shift

UPDATE (PUT/PATCH)

* Update a shift with PATCH

DELETE

* Delete a shift
