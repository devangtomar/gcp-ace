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

   1. Filestore : NFS file server (Store data from running application)

   2. Persistent Disks : Durable block storage for instances. Used by VM.
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



GitHub repo for follow along : <https://github.com/antonitz/google-cloud-associate-cloud-engineer>
🔗 Get your Free Practice and Downloadable Cheatsheets: <https://www.exampro.co/gcp-ace>
More notes : <https://github.com/agakhil13/gcp_quick_notes>
