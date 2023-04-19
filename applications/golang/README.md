## Supported Golang Versions

The Golang APM should work well with latest 2 Golang stable releases.
You can check this with ...
```
go version
```

## Current Technical Approach

Our Golang APM  works based on
https://github.com/open-telemetry/opentelemetry-go &
https://github.com/open-telemetry/opentelemetry-go-contrib

We have customized this base package based on our product requirement. 
* Added new metrics from our end
* Set up data export rules, so that telemetry data can be forwarded to our Host Agent

## Roadmap

1. We are planning to support Hostless APM as well which can send data directly to Middleware without need of any host agent. 
This will help to monitor cloud based managed applications.