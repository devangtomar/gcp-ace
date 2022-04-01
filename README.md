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

GCP has 24 regions, 73 zones and 144 network edge locations

POP (Point of presence) : Edge network : Most closest to the customer/user

Note : Zones (smallest identity) --> region (n.o of zones together) --> multi-regions (Geo-redundant data, 2 or more regions)

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

4. Cloud DNS :

Google Cloud DNS

5. Advanced connectivity :
   1. Cloud VPN : through IPsec connection
   2. Direct interconnect
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

4. Cloud Billing budgets : Traack your actual google cloud spends

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

**Metworking in GCP**

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

- Backup and restore of persistent disk
- Global resource
- Incremental and automatically compressed
- Stored in regional or multi-regional location

**Deployment Manager :**

YAML, JSON and Jinja to deploy and destory resources

Deploy --> update --> delete

🚀 GitHub repo for follow along : <https://github.com/antonitz/google-cloud-associate-cloud-engineer>

🔗 Get your Free Practice and Downloadable Cheatsheets: <https://www.exampro.co/gcp-ace>
