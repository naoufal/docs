# Network Projects Index

Shows projects that developers can apply to for a network.

## Path

`GET /networks/{ID}/projects.{FORMAT}`

## Auth

- authentication
- authorization

## Arguments

- `{ID}`: The ID of the network. This resource is authorized by the API key and will be provided when an API
key is requested

## Options

*None*

## Example

Request:
```
curl https://app.crew.co/api/networks/40/projects.json \
   -u 12345:
```

Response:
```
{
  [
    {
      "access_code": "rvvg02vf",
      "type": "app",
      "subtype": "iphone",
      "budget": {
        "amount": 5000,
        "type": "fixed",
        "hours": 0,
        "rate": 0
      },
      "location": [],
      "description": "New app description",
      "submission_date": "2016-06-06T12:46:31-0400",
      "url": "http://crew.dev/app?content=/projects/ajax_content/rvvg02vf"
    },
    {
      "access_code": "tw0mxuix",
      "type": "website",
      "subtype": "ecommerce",
      "budget": {
        "amount": 2500,
        "type": "hourly",
        "hours": 25,
        "rate": 100
      },
      "location": [
        "New York"
      ],
      "description": "New web app",
      "submission_date": "2016-06-06T12:47:00-0400",
      "url": "http://crew.dev/app?content=/projects/ajax_content/tw0mxuix"
    }
  ]
}
```
