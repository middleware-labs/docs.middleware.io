## Supported PHP Versions

The PHP APM should work well with php version above 8.0.
You can check this with ...
```
php -v
```

## Current Technical Approach

Our PHP APM  works based on https://github.com/open-telemetry/opentelemetry-php

We have customized this base package based on our product requirement. 
* Added new metrics from our end
* Adding severity based logging support ... (In progress)
* Set up data export rules, so that telemetry data can be forwarded to our Host Agent

## Roadmap

1. We are planning to support Hostless APM as well which can send data directly to Middleware without need of any host agent. 
This will help to monitor cloud based managed applications.

