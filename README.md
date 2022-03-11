# Topology Spread Constraints

The attached Kubernetes resource yaml file demonstrates topology constraints. For conceptual details please refer to the following URL:

https://kubernetes.io/docs/concepts/workloads/pods/pod-topology-spread-constraints/

Topology constraints should be considered a best practices for enabling application resiliency when deploying OpenShift on cloud providers offering multiple availability zones. Add the topologySpreadConstraints clause to any deployment specification requiring high-availability. An example of doing so is presented in the attached Kubernetes resource yaml file.

Before deploying the webapp.yaml file be sure to create a service account (sa-with-anyuid) and assign it the anyuid SCC. This is required for the pod to run.

When running this you can scale the number of replicas and watch their distribution across nodes (oc get pods -o wide) to validate that pods are being optimally distributed.
