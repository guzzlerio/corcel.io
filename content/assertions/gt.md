---
date: 2016-08-24T21:18:21+01:00
title: Greater Than
category: Assertions
tags: [assertions]
menu:
  main:
    name: Greater Than
    parent: Assertions
---

## Usage:

```yaml
assertions:
    - type: GreaterThan
      key: http:response:headers:Content-Length
      expected: 512
```
