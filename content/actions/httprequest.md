---
date: 2016-08-24T21:18:21+01:00
title: HttpRequest
category: Actions
tags: [actions, http]
menu:
  main:
    name: HttpRequest
    parent: Actions
---

## Description
The HttpRequest is used for all types of HTTP requests and supports the full list of methods (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`)

By default the `Content-Type` header is set to `application/json`.

## Properties

* `url`
* `method`
* `headers`
* `body`

## Keys available for assertion

Keys are prefixed with `urn:http`

* `request:error`
* `request:url`
* `request:headers`
* `response:status`

