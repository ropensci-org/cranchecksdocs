---
weight: 10
title: Root
output: 
  html_document:
    keep_md: true
---



# Root

This path redirects to /heartbeat

```shell
curl https://cranchecks.info/ | jq .
```
```yaml
HTTP/2 302 
access-control-allow-methods: HEAD, GET
access-control-allow-origin: *
cache-control: public, must-revalidate, max-age=60
content-type: application/json; charset=utf8
location: https://cranchecks.info/heartbeat
server: Caddy
x-content-type-options: nosniff
content-length: 0
date: Mon, 22 Mar 2021 13:00:37 GMT

```
