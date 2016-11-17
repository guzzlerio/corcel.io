---
date: 2016-08-24T16:27:03+01:00
title: Getting Started
menu:
  main:
    weight: 2
    name: Getting Started
    parent: Setup
---

To get started create a web server using a simple node.js script.

Add the following to a file called **server.js**

```javascript
const http = require('http');
const url = require("url");
const hostname = 'localhost';
const port = 1337;

http.createServer((req, res) => {
      res.writeHead(200, { 'Content-Type': 'text/plain' });
            res.end();
            
}).listen(port, hostname, () => {
      console.log(`Server running at http://${hostname}:${port}/`);
      
});
```

Next create a [URL file](/usage/using-a-url-file) called **urls.txt** and paste the following lines inside:

```txt
http://localhost:1337/people
http://localhost:1337/principles
http://localhost:1337/practices
http://localhost:1337/processes
```

Start your node.js web server with the following command:

```shell
node server.js
```

Inside a separate terminal invoke **corcel** ensuring you are in the same directory as the **urls.txt** file.

```shell
corcel run --duration 10s --workers 2 --summary urls.txt
```

Once the test has finished you should see an output like the following:

```shell
╔═══════════════════════════════════════════════════════════════════╗
║                           Summary                                 ║
╠═══════════════════════════════════════════════════════════════════╣
║         Running Time: 10.002795047s                               ║
║           Throughput: 5263 req/s                                  ║
║       Total Requests: 52587                                       ║
║     Number of Errors: 0                                           ║
║         Availability: 100.0000%                                   ║
║           Bytes Sent: 2.4 MB                                      ║
║       Bytes Received: 7.3 MB                                      ║
║   Mean Response Time: 0.0730 ms                                   ║
║    Min Response Time: 0.0000 ms                                   ║
║    Max Response Time: 8.0000 ms                                   ║
╚═══════════════════════════════════════════════════════════════════╝
```

Corcel can be used currently with a [URL file](/usage/using-a-url-file) or a [Scenario File](/usage/using-a-scenario-file).

