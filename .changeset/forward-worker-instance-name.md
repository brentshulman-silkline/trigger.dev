---
"trigger.dev": patch
---

Kubernetes: expose the worker node name to task runs for telemetry

Task runs on Kubernetes now receive the `TRIGGER_WORKER_INSTANCE_NAME` environment variable (the name of the node the run is executing on). This lets your `trigger.config.ts` telemetry attach the node as an OpenTelemetry `host.name`, so run traces and logs are attributed to a host instead of being reported with no host.
