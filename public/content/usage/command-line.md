---
date: 2016-08-24T16:26:56+01:00
title: Command Line Options
menu:
  main:
    name: Command line options
    parent: Usage
---

## Commands

### `run`
Run a Corcel test. Can either be from a [scenario file](/usage/using-a-scenario-file) or a [url file](/usage/using-a-url-file).

### `server`
Server will start up a Corcel Http Server for use in distributed load tests. **This is not fully implemented at present**.

---

## Command line options

```--summary```

Outputs a summary of the test which includes the following information

- Running Time
- Throughput (requests per second)
- Total Requests
- Number of Errors
- Availability (Total Requests vs. Number of Errors)
- Bytes Sent
- Bytes Received
- Mean Response Time
- Min Response Time
- Max Response Time 

```--duration=0s```

Sets the length of time the test will last.  By default the test will run until all urls have been executed or an execution plan has been completed a single time.  See [Valid Timeunits](#valid-time-units) for the value of this option.

```--wait-time=0s```

Sets the length of time execution will wait between a url or a scenario step.  If multiple workers are configured this value will apply to each worker.  See [Valid Timeunits](#valid-time-units) for the value of this option.

```--workers=1```

Sets the number of concurrent workers to use to execute the test.

- If using a URL file each worker will visit every URL in the file (unless a duration is set)
- If using a Scenario file each worker will execute each step of each job

```--random```

Sets the selection of the URL or the Job to be random.

```--progress```

Sets the progress bar to use. Available options are: `none|bar|logo`

### <a name="valid-time-units">Valid Timeunits</a>

A duration string is a possibly signed sequence of decimal numbers, each with optional fraction and a unit suffix, such as "300ms", "-1.5h" or "2h45m". Valid time units are "ns", "us" (or "µs"), "ms", "s", "m", "h".
