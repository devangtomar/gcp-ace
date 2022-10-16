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





GitHub repo for follow along : <https://github.com/antonitz/google-cloud-associate-cloud-engineer>
🔗 Get your Free Practice and Downloadable Cheatsheets: <https://www.exampro.co/gcp-ace>
More notes : <https://github.com/agakhil13/gcp_quick_notes>
