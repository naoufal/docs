# Pagination

Pagination can be done on list requests. The default item count that is returned is 20, and the default page is the first
page of items. The maximum items that can be returned on a single request is 100. The following pagination parameters
are available:

|Parameter|Default value|
|---------|-------|
|page|1|
|limit|20|

## Paging Details

Pagination links are returned in the `Link` header, as per [RFC 5988][1].

### Example: pagination request

```
GET /api/resources.json?page=2&limit=40 HTTP/1.1 
```

### Example: pagination response

If you request page 2 and there are a maximum of 5 pages, the link header would look something like this (formatted
for readability):

```
Link: <https://app.crew.co/api/resources.json/?page=1>; rel="first",
      <https://app.crew.co/api/resources.json/?page=1>; rel="prev",
      <https://app.crew.co/api/resources.json/?page=5>; rel="last",
      <https://app.crew.co/api/resources.json/?page=3>; rel="next"
```

[1]: https://tools.ietf.org/html/rfc5988
