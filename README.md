#K8s_sheet

Kubernetes Workload Terminology:

Pod-The basic execution unit — a group of one or more containers with shared storage and network.
ReplicaSet-Ensures a specified number of identical pods are running at any given time. Used by Deployments.
Deployment-	Manages stateless applications. Automatically creates and manages ReplicaSets and Pods.
StatefulSet-	Manages stateful applications that require stable identity and persistent storage (e.g., databases).
DaemonSet-	Ensures a copy of a pod runs on every node (or some nodes). Used for monitoring agents, logging, etc.
Job-	Runs a one-time task to completion (e.g., data migration).
CronJob-	Runs Jobs on a schedule, like a cron task.
