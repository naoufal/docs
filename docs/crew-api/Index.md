# Crew API Documentation

> The API is currently under development and the endpoints and response structure may change.

The Crew API is a RESTful API. This means it returns appropriate response codes with messages, such as 403 for requesting
a resource that you are not authorized to request, and 200 for successful API responses. It also follows REST conventions
by routing to the resource based on the HTTP method used:

- Get a list: `GET /networks.json`
- Get a resource: `GET /networks/1.json`
- Update a resource: `POST /networks/1.json`
- Delete a resource: `DELETE /networks/1.json`

Note that not all of the above endpoints actually exist and are for illustration purposes only. Please refer to the
documentation for existing endpoints.

## Table of Contents

- [Authentication and Authorization](Authentication.md)

## Endpoints

The host and path for all API requests is: `https://app.crew.co/api`

- [`GET /networks/{id}`](networks/View.md)
- [`GET /networks/{id}/projects`](networks/projects/Index.md)

## Formats

The current supported formats are:

- `json`: JSON format

You can request a format by appending it to the endpoint path, e.g.

```
curl https://app.crew.co/api/{RESOURCE}.{FORMAT} \
   -u {API_KEY}:
```
