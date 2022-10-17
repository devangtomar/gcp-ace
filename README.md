**Introduction :**

5 characteristics of cloud :

   1. On-demand self service : provision resources automatically without human intervention
   2. Broad  Network access : available over internet
   3. Resource pooling : Sharing resources etc.
   4. Rapid Elasticity : Rapidily provision and de-provision any of the cloud resource
   5. Measured service : Resouce usage can be monitored/metered

**Cloud Deployment models :**

1. Public cloud : AWS, GCP and Azure (Using 2 or more -> Multi-cloud)
2. Private cloud : Cloud that exists on-premises (GCP has --> Anthos)
3. Hybrid cloud : Public + Private cloud
4. Hybrid environment/network : On-premise DC + public cloud

**Cloud service models :**

XaaS : Anything as a service

1. Traditional on-premises : You takecare of everything

2. DC hosted : DC is there.. rest you takecare

3. IaaS : Compute Engine (VM instances). You decide what Operating System and software need to install.

4. PaaS : Only your data and application. Rest all is taken care by vendor

   - App Engine - Fully managed, serverless platform. Languages - Go, Java, .NET, Node.js, PHP, Python Ruby.

5. SaaS : Vendor takes care of everything.

5. CaaS

   - Google Kubernetes Engine (GKE) - For deploying and managing containers.

6. FaaS :

   - Cloud Functions - Serverless execution environment.No need to provision any infra. Languages - JavaScript, Java, node.js, .NET, Python3, Go.
   - Cloud Run - Full Managed for containerized Applications.

**Google Cloud Global infrastructure :**

- GCP has 24 regions, 73 zones and 144 network edge locations

- POP (Point of presence) : Edge network : Most closest to the customer/user

- Note : Zones (smallest identity) --> region (n.o of zones together) --> multi-regions (Geo-redundant data, 2 or more regions)

**Compute service options :**

1. Compute engine : Virtual machines called instances. You can use pre-configured images using Google cloud marketplace.

2. GKE (Called as CaaS) : Google kubernetes engine : Container orchestration for automating deploying, scaling and managing containers. This uses computer engine instances as nodes in a cluster.

3. App Engine : Fully managed an serverless platform. Google scales and provision servers.

4. Cloud Functions : Serverless execution environment. Single purpose functions.

5. Cloud Run : Fully managed compute platform for deploying and scaling containerized applications quickly and securely.
Knows asa serverless for containers.

**Storage and Databases :**

1. Storage :

   1. Cloud storage : Object storage. Durability : 11 9's durability : 99.9999999999999%

      Google for content delivery and data lake

      - Storage classses :
          1. Standard : max availability. No limitation
          2. Nearline : Low-cost archival storage. Accessed < 1/month
          3. Coldline : Even Lower-cost archival storage. Accessed < 1/Quater
          4. Archival : Lowest cost archival storage. Accessed < 1/year

   2. Filestore : NFS file server (Store data from running application)

   3. Persistent Disks : Durable block storage for instances. Used by VM.
      Types :
         1. Standard
         2. Solid state (SSD and low latency)

2. Databases :

   1. SQL:
      1. Cloud SQL: Fully managed database service. Ex : PSQL, MySQL. Have high availability across zones.

      2. Cloud Spanner : Scalable relational database service. High availability across regions and globally

   2. NoSQL:
      1. Big Table : High throughput
      2. DataStore : For mobile, web and IOT apps and ACID transactions
      3. FireStore : Optimized for offline use
      4. MemoryStore : Redis and memcached.

**Networking services :**

1. VPC : Virtual private cloud
Virtualized network within Google Cloud.
Networks cannot be shared b/w projects.

2. Firewall and routes
   1. Firewall Rules : Govern traffic

   2. Routes : How traffic will be re-directed

3. Load balancing :
   1. HTTPS load balancing : Used across region
   2. Network load balancing : Used in same region

4. Cloud DNS : Google Cloud DNS

5. Advanced connectivity :
   1. Cloud VPN : through IPsec connection
   2. Direct interconnect : More expensive
   3. Direct peering
   4. Carrier peering

**Resource hierarchy :**

Access control policies are inherited by child

Domain level <-- Organization <-- Folders <-- Projects <-- Resource

1. Service level resources

    - Compute Instance VM's
    - Cloud storage buckets
    - Cloud SQL databases

2. Account level resources

   - Organization
   - Folders
   - Projects

Controlled by IAM : Identity access management

**Cloud Billing :**

1. Billing account : who pays for GCP resources

    Types : Self-service (online) & Invoiced (offline)

      Sub-accounts : For customer separation and management.

2. Payments profile : Store all payment methods.

    Types : Individual and Business (Cannot be changed afterwards)

**Cost management and budget alerts**

1. Committed use discounts (CUD's) :

    Discounted prices when you commit to using a minimum level of resources for a specified term.

    1 or 3 year commmitment.

    Commitment Types :

       1. Spend based

          - Minimum amount for a service (hours)
          - 25% for 1 year discounts - 52% discount on a 3 year
          - Available for : Cloud SQL + Google cloud Vmware engine
          - Applies to CPU and memory usage

       2. Resource based

         - Minimum amount for compute engine resources
         - Available for vCPU, memory, GPU and local SSD
         - 57% discount for most resources and 70% for memory optimized machine types
         - For use across projects

2. Sustained-use discounts

   - Automatic discounts for running computer engine resources a significant portion of the billing month

   - Applies to vCPUs and memory for most compute engine instance types

   - Includes VM's created by GKE

   - Upto 30% discounts

3. GCP pricing calculator : Quick estimate of what your usage will cost on Google cloud

4. Cloud Billing budgets : Track your actual google cloud spends

    Budget alert --> monitoring --> email --> budget alert recepents.

5. Cloud Pub/Sub : Programatically notification or to automate cost management tasks. Real time notifications etc.

**Export Billing data :**

Enables granular billing data to be exported automatically to BigQuery for detailed analysis

**Cloud SDK and CLI :**

Cloud SDK :

    Set of command lines tools to manage resource via terminal

    Ex : gcloud, gsutil, bq, kubectl

    You can use a user account or service account for using Cloud SDK and automating stuff.

**Limits and Quotas :**

Hard limit on how much of a particular google cloud resource your project can use.

Types :

   1. Rate quota : resets after specified time. Ex : API usage
   2. Allocation quota : Must be explicity released. Ex : Deleting GKE cluster.

How to view :

    1. Quotas page
    2. API dashboard

**Cloud IAM**

IAM : Policy + Bindings

Let's you manage access control by defining who, has what access, for which resource.

- Principle of least privilege - Apply only the minimal access level required for what's needed.
- Set policies at organization or project level rather than at the resource level.
- Grant roles for users or group at the folder level rather than at the project level.
- Grant roles to Google groups rather than individual users.

Types of roles :

   1. Primitive : Roles historically available in the GCP. Ex : Owner, editor and viewer
   2. Predefined : Finer grained access control than the primitive roles
   3. Custom : tailor permission to the needs of your org.

Conditions :

1. Time based conditions
2. Resource based conditions

**Service accounts :**

Bot account for automating tasks.

Types :

1. User managed account
2. Default account
3. Google managed account

Uses service account keys (For sign-in)

**Cloud Identity :**

IDaaS : Identity as a Service

GCDS : Google cloud directory sync : Acitve directory for GCP

**Networking in GCP**

1. **VPC** : Virtual private cloud

   - Virtualized network within GCP
   - A VPC is a global resource
   - Encapsulated within Project
   - Resource within VPC can commmunicate with one another using internal IPv4 addresses
   - Support only for IPv4 addresses
   - Each VPC contains a default network
   - Types :
     - Auto Mode (Automatic subnet)
     - Custom Mode (Custom subnet.. gives more control)

Connection of 1 VPC to another VPC : **VPC peering**

**VPC Firewall rules :**

Allows you to allow or block incoming and outgoing connections

**VPC Peering :**

- Private connectivity across 2 VPC networks
- Peer across the same or different projects and org
- Reduce network latency
- Increase network security
- Reduce network costs

**Shared VPC :**

Types :

1. Shared VPC
   - Allow org to connect different project with a single VPC network
   - There are a host and service project.. cannot be both
   - Standalone project are the one that doesn't connect with anything else.
2. Multiple hosts project (2 separate hosts attached)
3. Hybrid environment (On-prem with Cloud VPN)
4. Two tier web service

**VPC Flow logs :**

Real-time visibility into network throughput and performance. Useful for real-time security analysis.

**Cloud DNS :**

Host authoritative name server and allow authoritative DNS lookups (DNS as a service)

100% SLA

Host zones through managed name servers

   1. Public zones : visible to the internet
   2. Private zones : visible only within your network

**Compute engine :**

1. Virtual machine = Instance (IaaS)
2. Multiple instance sizes and types
3. Per second billing
4. Launched in a VPC network
5. Host is available in a zone
6. Multi-tenant host (cheap) or sole tenant node (expensive)

Machine configuration :

1. Cores (vCPU) memory
   1. predefined
   2. Custom

2. OS
   1. Public image : linux or windows
   2. custom image : private images
   3. marketplace : os + software

3. Storage
   1. perfomance Vs Cost
      1. Standard : HDD
      2. Balanced : alternative to SSD
      3. SSD
      4. Local SSD : Physically attached (swap disk)

**Compute engine machine types :**

Types :

1. General purpose
2. Compute optimized
3. Memory optimized

**Managing instances :**

Shielded VMs : Secure boot

**Compute engine billing :**

vCPUs and momory are billed separately

They are charged by the seconds with a minimum of 1 minute

Reservations :

- Ensuring resources are available for when you need it.
- Include sustained use and committed use discounts
- Apply only to compute engine, dataproc and GKE

**Discount types :**

1. Sustained use discounts

   - Auto discounts applied to vcpu and GPU and memory

2. Committed use discounts

    - Purchased 1 year or 3 year contracts in return for deeply discounted prices
    - Predicatable/steady state resources
    - 57% for most resources
    70% for memory optimized machine types

3. Preemptible VMs

   - 80% cheaper
   - Fixed pricing
   - Stops after Within 24 hours
   - No charge if < 10 mins
   - No live migration and auto-restart
   - Good for fault tolerant apps

**Storage fundamentals :**

1. Block storage
   1. Persistent disks
      1. Network storage
      2. independent
      3. resize while running
      4. encrypted
      5. upto 64TB in size
      6. **Use regional PD for zonal outage for backup and data redundancy**

   2. Local SSDs
      1. Physically attached
      2. Higher IOPS
      3. Data persists until instance is stopped or deleted.

**Persistent Disk Snapshots :**

- Backup andode restore of persistent disk
- Global resource
- Incremental and automatically compressed
- Stored in regional or multi-regional location

**Deployment Manager :**

YAML, JSON and Jinja to deploy and destory resources

Deploy --> update --> delete

**Cloud load balancer :**

Backend services : Defines how cloud load balancing distributes traffic

- Types of Load Balancer
  - HTTP(s) :
    - Types : Cross region load balancing and Content based load balancing
    - Layer 7 load balancer
    - Global, proxy based layer 7 load balancer behing a single external IP address

  - SSL Proxy
    - Reverse proxy load balancer that distributes SSL traffic coming from internet to VMs
    - Layer 4 load balancer
    - Support for TCP with SSL offload

  - TCP proxy
    - Reverse proxy load balancer that distributes TCP traffic coming from internet to VMs
    - Layer 4 load balancer

  - Network
    - Pass through load balancer tha distributes the TCP and UDP traffic to VMs
    - Not a proxy

  - Internal
    - Layer 4 load balancer
    - Internal load balancer b/w VM instances

**Instance Groups and Instance templates :**

Instance group is a collection of VMs which can controlled like 1 VM

Types of Instance groups : Manageed instance groups (MIGs) and Un-managed instance groups

MIGS : Can be used with : Preemptible VMs, containers, Network and subnet

Instance templates : Resource used to create VM instances and MIGs
It cannot update or change existing instance template

**Introduction to containers :**

Container registry : Single place to store and manage your docker images. Ex: DockerHub

**GKE and kubernetes concepts :**

K8s : Orchestration platform for containers
Used for automate, schedule and run containers
Managed by CNCF (Cloud native computing foundation)

GKE : Google Cloud kubernetes engine

Features :

1. Cloud load balancing
2. Node pools
3. automatic scaling
4. automatic upgrades
5. node auto-repair
6. logging and monitoring

Cluster :

Foundation of GKE

Contains :

1. Control plane : responsible for scheduling and management

Parts of control plane :

   1. Cluster IP
   2. kube scheduler
   3. kube controller manager
   4. cloud controller manager
   5. ETCD

   2. 1 or more nodes : Node runs containerized apps and is responsible for Docker runtime

kubectl : CLI for kubernetes

Surge upgrade : control the number of nodes GKE can upgrade at a time. Ex : max-surge-upgrade, max-unavailable-upgrade

**GKE storage options :**

Types :

1. Databases storage :

   1. Cloud SQL
   2. Cloud Spanner
   3. DataStore

2. NAS :

   1. Filestore

3. Object storage :

   1. Cloud storage

4. Block storage :

   1. Persistent disk

**Cloud VPN :**

   Connects your peer network to your VPC network through an IPsec VPN connection

   IPsec tunnel over the public internet

   Cloud VPN is a regional service
   Site to site VPN only (no site to client)
   Allows private google access for on-premises hosts
   Support up to 3 Gbps per tunnel

   Types of cloud VPN :

   1. Classic VPN : 99.9% SLA (3 9's SLA) , Static and dynamic routing, 1 ext IP for 1 interface, Deprecating functionality in 2021

   2. HA VPN : 99.99% SLA (4 9's SLA), Dynamic ruting, 2 ext IPs for 2 interfaces, new default VPN

**Cloud interconnect :**

   Low latency, highly available connection b/w your on-premises and GCP VPC n/w

   Directly accessiible internal IP address : private google access

   Does not traverse the public internet

   Not encrypted

   Expensive

   Dedicated connection

   Types :

   1. Direct intnerconnect
   2. Partner internconnect

**App engine overview :**

   1. Fully managed, serverless platform to develop and host web apps
   2. PaaS service
   3. Autoscaling based on loads

**Cloud functions :**

   Serverless. FaaS. You won't see the apps unlike app engine

   Event driven

**Cloud storage :**

   1. Object storage.
   2. For pictures and videos and not operating systems

   Based on location :

      1. Region
      2. Dual-region
      3. Multi-region

   Types :

      Hot data :

         1. Standard (max availability)
         2. Nearline (Low cost for infrequently accessed data. 30 day min storage duration)

      Cold data :

         1. Coldline (90 days min storage duration)
         2. Archive (365 day min storage duration)

**Cloud SQL :**

   Fully managed, relational database service (RDBMS)

   DBaaS (Database as a service)

   Low latency, transactional, reational db workloads

   High availability

**Cloud Spannar :**

   Different from Cloud SQL.

   It's horizontally scalable and strongly consistent

   Supportt schemas, ACID transactions and SQL queries

**NoSQL databases :**

   Types :

   1. Cloud BigTable (TB to PetaByte scale workload) : Hadoop etc.
   2. Cloud Datastore : Document database (Being retired in favor of cloud firestore in 2021)
   3. Firestore for firebase : Serverless amd store data in documents.
   4. MemoryStore : for Redis and memcached in-memory data store for cache.

**Big Data overview :**

   Services :

      1. BigQuery : Fully managed, petabyte scale, low cost analytics data warehouse
      2. Pub Sub : Fully managed real time messaging service. Send and receive messages b/w independent application
      3. Composer : (Built on APache airflow) Fully managed workflow orchestration service... used for automating workflows..
      4. Dataflow : (Used for ETL) Fully managed processing service for executing Apache beam pipelines for batch and realtime data streaming.
      5. DataProc : Spark and hadoop service. Can be used to replace on-prem hadoop infrastructure.

**Dataproc vs dataflow**

Dataflow : serverless
Dataproc : managed

**Rest of the services :**

- BigQuery - For analysis of large data.

- Pub/Sub - Queue for notification.

- Composer - Built on Apache Airflow, workflow orchestration service

- Dataflow - Apache beam pipelines for batch and realtime datastream,for ETL. Serverless. Cloud Dataflow is a stream and batch processing service

- Dataproc - Run hadoop spark on google cloud. Fully managed instance.

**Machine learning :**

   Services :

         - Datalab - Tool for machine learning and visualization.

         - Cloud Data Fusion - Cloud Data Fusion is a managed service that is designed for building data transformation pipelines.

         - Dataprep - Serverless. Cloud Dataprep is used to prepare data for analytics and machine learning.

         - Sight
           - Vision : For images (clasify images and hand written text data).
           - Video Intelligence : For videos (recognize a vast number of objecta and streaming videos).

         - Language
           - Natural Language : (Derive insight using unstructred text)
           - Translation : (Enables you to translate between languages).

         - Conversation -
           - Dialog Flow : chat bots
           - Speech to text
           - text to speech.

         - Auto ML - Fully managed service to build ML product with less knowledge.

**Operation Suite :** (Previously knows as Stackdriver)

- Tool for logging, monitoring and application diagnostics. Can also get connect to AWS.

Types :

- Cloud Monitoring - Cloud Monitoring is used for collecting and view metrics on resource performance.
- Cloud Logging - who did what,where and when. Connection records can be viewed in Cloud Logging.
- Error Reporting - Alerts you when new application error occurs.

Application performance management :

- Debugger - Cloud Debugger is used by developers to identify and correct errors in code.
- Trace - Cloud Trace is used to understand performance in distributed systems.
- Profiler - Gather CPU and memory usage from your application.

🚀 GitHub repo for follow along : <https://github.com/antonitz/google-cloud-associate-cloud-engineer>

🔗 Get your Free Practice and Downloadable Cheatsheets: <https://www.exampro.co/gcp-ace>
