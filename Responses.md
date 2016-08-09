# Responses

## Successful Responses

Successful responses return an HTTP status of 200. Please note, these responses are not enveloped.

### Example: response

This is an example of a response for a single resource, such as `GET /api/resources/1.json`. It will return the object
you request.

```
HTTP/1.1 200 Ok

{
    "id": 1,
    "name": "A resource",
    "created": "2016-03-29T20:34:47-0400"
}
```

### Example: list response

This is an example of a response for multiple resources, such as `GET /api/resources.json`. It will return an array of
objects that were requested.


```
HTTP/1.1 200 Ok

[
    {
        "id": 1,
        "name": "A resource",
        "created": "2016-03-29T20:34:47-0400"
    },
    {
        "id": 2,
        "name": "Another resource",
        "created": "2016-03-29T20:34:47-0400"
    },
    {
        "id": 3,
        "name": "A third resource",
        "created": "2016-03-29T20:34:47-0400"
    }
]
```

## Error Responses

Errors are always keyed with an `errors` key, which contains an array of errors. The error format follows the [JSON API][1]
specification for errors.

### Example: missing endpoint

Below is an example of an error response for a missing endpoint. The response itself will also have a 404 status.

```
HTTP/1.1 404 Not Found

{
    "errors":
    [
        {
            "status": "404",
            "title": "Not Found"
        }
    ]
}
```

### Example: validation errors

If, when submitting a `POST` request, the request may not validate. In this case, you will receive an array of validation
errors. These errors will contain a [JSON pointer][2] to the field that contained the error.

```
HTTP/1.1 400 Bad Request

{
    "errors": [
        {
            "source": { 
                "pointer": "/name" 
            },
            "detail": "Name must not be empty"
        },
        {
            "source": { 
                "pointer": "/budget" 
            },
            "detail": "Budget must be number greater than 0"
        }
    ]
}
```

[1]: http://jsonapi.org/format/#error-objects
[2]: https://tools.ietf.org/html/rfc6901
