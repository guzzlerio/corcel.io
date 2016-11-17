---
date: 2016-08-24T21:18:21+01:00
title: Regex
category: Extractors
tags: [extractors, regex]
menu:
  main:
    name: Regex
    parent: Extractors
---

## Usage:

```yaml
extractors:
    - type: Regex
      name: isbn
      key: http:response:body
      xpath: \\d+
```
