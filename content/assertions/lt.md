---
date: 2016-08-24T21:18:21+01:00
title: Less Than
category: Assertions
tags: [assertions]
menu:
  main:
    name: Less Than
    parent: Assertions
---

## Usage:

```yaml
assertions:
    - type: LessThan
      key: http:response:headers:Content-Length
      expected: 512
```
