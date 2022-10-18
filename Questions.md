**GCP data transfer services :**

1. Storage transfer service :
   1. for data more than 1 TB
   2. Enough bandwidth to meet project dealine
   3. Mainly used for moving online data to Google Cloud Platform network. Not the ideal option

2. Transfer appliance
   1. Not enough bandwidth to meet your project deadline


**GKE :**

DaemonSet : is a controller similar to ReplicaSet that ensures that the pod runs on all the nodes of the cluster

StatefulSet : is used for Stateful applications, each replica of the pod will have its own state, and will be using its own Volume

Deploy the new version in the same application and use the --splits option to give a weight of 99 to the current version and a weight of 1 to the new version.

--splits=SPLITS,[SPLITS,...]

**Create bucket command**

gsutil mb

**Service account**

You can create a private key for them.

**IAM role**

creator : writer

admin : write, delete etc.

**Increase ram in comuter engine**

To increase RAM... shutdown VM and then increase RAM/memory

**Simple rule**

 if metrics then Monitoring, if Auditing then Logging