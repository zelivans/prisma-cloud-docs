Retrieves image scan reports.

This endpoint maps to the image table in **Monitor > Compliance > Images > Deployed** in the Console UI.

### cURL Request

Refer to the following cURL command that retrieves a compact scan report for all images:

```
$ curl -k \
  -u <USER> \
  -H 'Content-Type: application/json' \
  -X GET \
  "https://<CONSOLE>/api/v<VERSION>/images"
```

Refer to the following cURL command that retrieves a compact scan report for an Ubuntu image:

```
$ curl -k \
  -u <USER> \
  -H 'Content-Type: application/json' \
  -X GET \
  "https://<CONSOLE>/api/v<VERSION>/images?name=https://<REPO-URL>/ubuntu:latest&compact=true"
```
The name query is synonymous with the filter images text field in the Console UI.

Refer to the following cURL command that retrieves the scan report for an image with the matching SHA-256 hash:

```
$ curl -k \
  -u <USER> \
  -H 'Content-Type: application/json' \
  -X GET \
  "https://<CONSOLE>/api/v<VERSION>/images?id=sha256:d461f1845c43105d7d686a9cfca9d73b0272b1dcd0381bf105276c978cb02832"
```

A successful response returns the image scan reports.
