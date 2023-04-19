## Supported Python Versions

The Python APM should work well with Python 3.0 and higher.
APM is also collecting expected data for Python 2.7, but we recommend to upgrade to Python 3.0 for more stability, if possible.

You can check this with ...
```
python --version
```

## Current Technical Approach

Our Python APM  works based on https://github.com/open-telemetry/opentelemetry-python

We have customized this base package based on our product requirement. 
* Added new metrics from our end
* Added severity based logging support
* Set up data export rules, so that telemetry data can be forwarded to our Host Agent

## Roadmap

1. We are planning to support Hostless APM as well which can send data directly to Middleware without need of any host agent. 
This will help to monitor cloud based managed applications.

