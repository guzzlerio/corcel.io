---
date: 2016-08-24T21:05:40+01:00
title: Using a Scenario File
menu:
  main:
    name: Using a Scenario File
    parent: Usage
---

An example scenario file :

```yaml
---
  name : The plan
  workers : 5
  waitTime : 1500
  duration: 10s
  random : true
  parallelJobs : true
  jobs:
    -
      name : Register a user
      steps:
        -
          name: Step number 1
          action:
            type : HttpRequest
            requestTimeout : 150
            method : GET
            url : http://localhost:1337/success
            headers:
                content-Type: application/json
          assertions:
            -
              type: ExactAssertion
              key: http:response:status
              expected: 200
```
