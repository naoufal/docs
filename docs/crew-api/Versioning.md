# Versioning

You can request different versions of the API in the `Crew-Api-Version` header. If you do not request a version, the
first available version of the API will be served. It is recommended that you pass the version header in all requests.
Versions are in a YYYY-MM-DD format.

The current version is `2016-08-02`.

## Example request

```
GET /api/resources.json HTTP/1.1
Crew-Api-Version: 2016-08-02
```
