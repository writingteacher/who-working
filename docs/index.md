---
layout: page
---

# Who's Working API Documentation

### Turn your app into a staffing solution

Who's Working is a cloud service that helps your shift managers find trained part-time workers and fill staffing positions. It's an ideal tool for quick service operations that experience last-minute staff changes. The lightweight API provides access to a list of trained part-time workers who might be available on short notice for a restaurant shift. The Who's Working API uses REST and returns HTTP response codes and responses encoded in JSON.

There are two resources.

**Workers** - A record for each part-time worker who agreed to have their name and contact information added to the Who's Working service. The Workers resource includes endpoints to create, retrieve, update, and delete user information. In Version 1, store managers create worker records. In version 2, workers will be able to create and update their own records (subject to store manager review and approval).

**Shifts** - Available shifts in the restaurant created by the shift manager. Each shift describes the location, day and time, shift length, and warnings. The Shifts resource includes endpoints to create, retrieve, update, and delete shift records.

## Authentication

The Who's Working app uses [Basic Authentication](api/basic_auth.md).

## Before you start

The quickstart tasks and tutorial listed below are designed to run on your development system with Postman. Before running the quickstart or tutorial, you need to set up your system. The good news is that you only need to complete the setup once per development system.

* [Before you start](tutorials/before-you-start-a-tutorial.md)

After your system is ready, open the quickstart or tutorial and learn how to perform common tasks.

## Quickstart

This [quickstart](api/quickstart_working.md) article provides all the information you need to begin using Who's Working to fill last minute staffing vacancies. Expect to complete the quickstart tasks and make your first API call in about ten minutes.

## Tutorials

#### Shifts

* [Update a shift](tutorials/update-a-shift.md)
* Create a shift
* Edit a shift
* Delete a shift
* Get a shift by a property

#### Workers

* Create a new worker
* Update a specific worker's information
* Delete a worker
* Get a worker by a property

## API reference docs

Click a link to read detailed descriptions of the service's resources. The API reference docs refer to a `{server_url}` when they refer to the URL of a resource. The `{server_url}` value depends on the installation of the service. When running a local test, the `{server_url}` is generally `http://localhost:3000`.

* [Shifts resources](api/shifts-resources.md)
* [Workers resources](api/workers-resources.md)
