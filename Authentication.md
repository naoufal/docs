# Authentication

The Crew API uses basic auth for authentication. It uses the API key as the `username` with no `password`.

With your API key, authenticating requests is simple. Here's an example using Curl:

```
curl https://app.crew.co/api/{RESOURCE} \
   -u <API_KEY>:
```

## Example authentication error response

```
{
"errors":
    [
        {
            "status": "401",
            "title": "Unauthorized"
        }
    ]
}
```
