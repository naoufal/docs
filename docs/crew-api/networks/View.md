# Networks View

Shows information for a network.

## Path

`GET /networks/{ID}.{FORMAT}`

### Auth

- authentication
- authorization

## Arguments

- `{ID}`: The ID of the network to view. This resource is authorized by the API key and will be provided when an API
key is requested

## Options

*None*

## Example

Request:
```
curl https://crew.co/api/networks/40.json \
   -u 12345:
```

Response:
```
{
  "network": {
    "id": 40,
    "name": "My Crew Network",
    "created": "2016-01-17T01:21:29-0500",
    "project_count": 6,
    "active_dev_count": 1
  }
}
```
