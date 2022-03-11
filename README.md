# Topology Spread Constraints

The attached Kubernetes resource yaml demonstrates topology constraints. For conceptual details please refer to the following URL:

https://kubernetes.io/docs/concepts/workloads/pods/pod-topology-spread-constraints/

Topology constraints should be considered a best practices when deploying OpenShift on cloud providers offering multiple availability zones.

Before deploying the webapp.yaml file be sure to create a service account (sa-with-anyuid) and assign it the anyuid SCC. This is required for the pod to run.

