---
date: 2016-08-24T21:18:21+01:00
title: Greater Than or Equal
category: Assertions
tags: [assertions]
menu:
  main:
    name: Greater Than or Equal
    parent: Assertions
---

## Usage:

```yaml
assertions:
    - type: GreaterThanOrEqual
      key: http:response:headers:Content-Length
      expected: 512
```
