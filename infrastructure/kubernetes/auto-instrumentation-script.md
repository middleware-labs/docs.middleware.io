# Auto-Instrumentation in Kubernetes

Our Kubernetes auto-instrumentation script ...
* Monitors your Kubernetes cluster as an Infrastructure
* Collects distributed traces for all the applications running inside your cluster

## How Auto-Instrumentation Works

Once user hits the Kubernetes Auto-Instrumentation script, the script will install a helm chart in the cluster, which will ...

1. Detect programming languages for all the pods running inside your cluster. (Refer Language Support section at bottom)
2. Install Opentelemetry auto-instrumentation libraries in all the pods that user wants to monitor.
3. Install a Daemonset to monitor the performance of all the K8s components. Ex. Nodes, Pods, Containers, etc.
4. Send all infrastructure + application data to Middleware backend !

## Language Support

| Language      | Version Support     |
| --- | --- |
|Node.js| Details coming soon|
|Python| Details coming soon|
|Java| Details coming soon|
|C#| Details coming soon|
|Golang| Details coming soon|

**Note: Golang distributed tracing support is made possible by eBPF**