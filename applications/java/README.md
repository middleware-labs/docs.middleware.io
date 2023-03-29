## Supported Java Versions

The Java APM should work well with php version above 8.0.
You can check this with ...
```
java --version
```

## Current Technical Approach

Our Java APM  works based on https://github.com/open-telemetry/opentelemetry-java-instrumentation

We have customized this base package based on our product requirement. 
* Added new metrics from our end
* Added severity based logging support
* Set up data export rules, so that telemetry data can be forwarded to our Host Agent

## Roadmap

1. We are planning to support Hostless APM as well which can send data directly to Middleware without need of any host agent. 
This will help to monitor cloud based managed applications.