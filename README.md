# Description
Here we list the minimum requirements that a repository must fulfill.

# Requirements
* [JWT] Authentication
* A CRUD implementation for a root model
* A CRUD for Relationships

All CRUD implementations must implement:
* At least one *Create* endpoint must be available via a *POST* request
* At least one *Read* endpoint must be available via a *GET* request
* At least one *Update* endpoint must be available via a *PUT* request
* At least one *Delete* endpoint must be available via a *DELETE* request

The following verb' implementations are optional, but if done, should behave as follows:
* *HEAD*: ???
* *OPTIONS*: ???
* *PATCH*: allow for partial content update - *PUT* is used to completely replace the endpoint contents

# Database
All implementations must use only the framework's tool to access the database.

Creating the tables, seeding data, queries etc. all must be as agnostic as possible.

# Endpoints
A list of some basic endpoints that must be implemented:

## Authentication
* `POST /login`

## Main resource
* `GET /contacts`
* `GET /contacts/:id`
* `POST /contacts`
* `PUT /contacts/:id`
* `DELETE /contacts/:id`

## Sub-resource / relationship
> Question: must the sub-resource stay under its parent endpoint?

* `GET /contacts/:id/address`
* `GET /contacts/:id/address/:addr_id`
* `POST /contacts/:id/address`
* `PUT /contacts/:id/address/:addr_id`
* `DELETE /contacts/:id/address/:addr_id`

# Responses
[TBD](https://github.com/RESTBench/requirements/issues/1)

# Documentation
[TBD](https://github.com/RESTBench/requirements/issues/2)

# Tests
[TBD](https://github.com/RESTBench/requirements/issues/3)

# CI
[TBD](https://github.com/RESTBench/requirements/issues/4)


  [JWT]: https://jwt.io/
