---
date: 2016-09-20T14:46:45+01:00
title: Using a URL File
menu:
  main:
    name: Using a URL File
    parent: Usage
---

The format of the lines in the URL file follows the CURL arguments. The arguments currently support include:

* `-H` to specify a header
* `-X` to specify the HTTP verb
* `-d` to specify the data to send. the @ symbol can be used to prefix a file path

An example line:

```curl
http://localhost:8000 -X POST -H "Content-type: application/json" -H "Accept: application/json" -d '{"name":"talula"}'
```
