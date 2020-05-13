---
weight: 20
title: History
output: 
  html_document:
    keep_md: true
---



# History

Get link for compressed json file of historical CRAN checks results for a given date - across all packages.

On success, you'll get a 302 redirect, with a temporary link (expires in 15 minutes) for the Amazon S3 file in the Location response header.

Follow redirects to make sure that you are redirected to the link.

For historical data _by package_ refer to the [package history endpoint](#packages-by-name-history).

If you don't follow redirects, you'll get a JSON body telling you to redirect to the Location header link.

```shell
curl https://cranchecks.info/history/2020-04-01 | jq .
```
```yaml
HTTP/2 302 
access-control-allow-methods: HEAD, GET
access-control-allow-origin: *
cache-control: public, must-revalidate, max-age=60
content-type: application/json; charset=utf8
location: https://cchecks-history.s3.us-west-2.amazonaws.com/2020-04-01.json.gz?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIE65F6ZPF3JF7JTA%2F20200513%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200513T071825Z&X-Amz-Expires=900&X-Amz-SignedHeaders=host&X-Amz-Signature=4c5c48558090c878e5ac7cb0dde3fef7af0ef6fc77acb90024626251f69fd9ba
server: Caddy
x-content-type-options: nosniff
content-length: 101
date: Wed, 13 May 2020 07:18:25 GMT

```
```json
{
    "error": null,
    "message": "you hit a redirect. use the link in 'Location' header; or follow redirects"
}
```
