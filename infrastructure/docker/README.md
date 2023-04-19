## Supported Machines

We have created docker distributions using https://github.com/marketplace/actions/build-and-push-docker-images

All the OS that supports docker should also support our docker based agent.

This is applicable on both x86 & ARM based machines, as we are using multi-platform builds.

## Current Technical Approach

In order to collect host level details, our docker agent works on host network mode.

For log reading, the docker agent uses volume binding.


## Roadmap

1. Current docker installation bash script works well with Linux + Mac machines. We will be making this script adaptable for Windows machines as well.
