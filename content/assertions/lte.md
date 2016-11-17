---
date: 2016-08-24T21:18:21+01:00
title: Less Than or Equal
category: Assertions
tags: [assertions]
menu:
  main:
    name: Less Than or Equal
    parent: Assertions
---

## Usage:

```yaml
assertions:
    - type: LessThanOrEqual
      key: http:response:headers:Content-Length
      expected: 512
```
