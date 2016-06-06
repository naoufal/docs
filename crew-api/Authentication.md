# Authentication and Authorization

## Authentication

The Crew API uses basic auth for authentication. It uses the `username` as the API key, similar to how the
[Stripe](https://stripe.com) API authenticates.

With your API key, authenticating requests is simple. Here's an example using Curl:

```
curl https://crew.co/api/{RESOURCE} \
   -u <API_KEY>:
```

### Example authentication error response

```
{
  "message": "Unauthorized",
  "url": "/api/networks/40/projects.json",
  "code": 401
}
```

## Authorization

Most authorization is provided by the API key, that is, the API key is linked to objects and child objects. Accessing
other objects will return an Authorization error.

### Example authorization error response

```
{
  "message": "You are not authorized to access that location.",
  "url": "/api/networks/41/projects.json",
  "code": 403
}
```
