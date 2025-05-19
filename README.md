#K8s_sheet

Kubernetes Workload Terminology:

Pod-The basic execution unit — a group of one or more containers with shared storage and network.

ReplicaSet-Ensures a specified number of identical pods are running at any given time. Used by Deployments.

Deployment-	Manages stateless applications. Automatically creates and manages ReplicaSets and Pods.

StatefulSet-	Manages stateful applications that require stable identity and persistent storage (e.g., databases).

DaemonSet-	Ensures a copy of a pod runs on every node (or some nodes). Used for monitoring agents, logging, etc.

Job-	Runs a one-time task to completion (e.g., data migration).

CronJob-	Runs Jobs on a schedule, like a cron task.


🧱 Core Kubernetes Storage Terminology

Volume-	A directory accessible to containers in a Pod. Lives as long as the Pod. Can be backed by disk, NFS, etc.

emptyDir-	A temporary volume that exists only while the Pod is running. Data is lost after pod restart.

hostPath-	Mounts a file or directory from the host node into a Pod. Good for testing but not recommended in production.

PersistentVolume (PV)-	A cluster-wide storage resource provisioned by an admin or dynamically. Represents physical storage.

PersistentVolumeClaim (PVC)-	A request for storage by a user. Binds to a PV that satisfies the request.

StorageClass-	Defines different classes of storage (e.g., fast SSDs, slow HDDs). Supports dynamic provisioning of PVs.

Volume Mount-	Specifies where the volume should be mounted inside a container.

CSI (Container Storage Interface)-	A standard interface to provision and manage volumes from external storage systems.

Dynamic Provisioning-	Automatically creates PVs on demand when a PVC is created, using a StorageClass.
