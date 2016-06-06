# Crew.co API Documentation

The Crew API is a RESTful API. It is currently under development and the endpoints and response structure may change.

## Table of Contents

- [Authentication and Authorization](Authentication.md)

## Endpoints

The host and path for all API requests is: `https://crew.co/api`

- [/networks/{id}](networks/View.md)
- [/networks/{id}/projects](networks/projects/Index.md)

## Formats

The current supported formats are:

- `json`: JSON format

You can request a format by appending it to the endpoint path, e.g.

```
curl https://crew.co/api/{RESOURCE}.{FORMAT} \
   -u {API_KEY}:
```
