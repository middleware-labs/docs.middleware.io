## Supported Node.js Versions

The Node.js APM should work well with node version above v8.12.0.
Because the some of the APM functionality works on `perf_hooks`.

You can check this with ...
```
node --version
```

## Current Technical Approach

Our Node.js APM  works based on https://github.com/open-telemetry/opentelemetry-js

We have customized this base package based on our product requirement. 
* Added new metrics from our end
* Added severity based logging support
* Set up data export rules, so that telemetry data can be forwarded to our Host Agent


## Roadmap

1. We are planning to support Hostless APM as well which can send data directly to Middleware without need of any host agent. 
This will help to monitor cloud based managed applications.

