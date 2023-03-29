## Support for Cloudflare Worker

The Cloudflare worker APM should work well with wrangler version equal or above 2.2.2.
You can check this with ...
```
wrangler version
```

## Current Technical Approach

The Cloudflare APM is inspired from
https://www.npmjs.com/package/opentelemetry-sdk-workers

We have customized this base package based on our product requirement. 
* Added new metrics from our end
* Added severity based logging support
* Set up data export rules, so that telemetry data can be forwarded to our Host Agent

## Roadmap

1. We are planning to support Hostless APM as well which can send data directly to Middleware without need of any host agent. 
This will help to monitor cloud based managed applications.