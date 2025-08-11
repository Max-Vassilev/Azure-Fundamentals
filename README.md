# Azure Fundamentals - notes for certification

## 1. Benefits of Cloud Computing
1. **High Availability** – Avoid obvious downtime sources.  
2. **Scalability** – Add resources manually when needed.  
3. **Elasticity** – Automatically add/remove resources on demand.  
4. **Reliability** – Keep systems running during failures.  
5. **Predictability** – Consistent performance and cost.  
6. **Security** – Access controls, encryption, and protection of data.  
7. **Governance** – Enforce rules, auditing, and cost limits.  
8. **Manageability** – Easily monitor and control resources.  

## 2. Cloud Service Types
- **SaaS** – Ready-to-use software.  
- **PaaS** – Simplifies app deployment without managing servers (not event-driven).  
- **IaaS** – Virtual servers; you manage OS and apps.  
- **Serverless** – Event-driven; runs code only when needed, no server management.  

## 3. Core Azure Architecture
- **Region Pairs** – Two linked regions for backup, DR, and high availability.  
- **Availability Zones (AZ)**  
  - **Zonal Services** – Single zone; outage stops service.  
  - **Zone-Redundant Services** – Across zones; auto failover.  
  - **Always Available Services** – Replicated across regions.  
- **Resource Groups** – Logical containers; can hold resources from any region; region-bound; assign permissions at group level.  
- **Subscriptions** – Free trial, pay-as-you-go, Enterprise Agreement, or free credits. Can separate departments.  
- **Management Groups** – Optional; group subscriptions for centralized policies.  

## 4. Compute & Networking
- **VM Scale Sets** – Auto-scaling VMs (up to 1000).  
- **Availability Sets** – Spread VMs for fault isolation.  
- **Proximity Groups** – Place VMs close for low latency (less availability).  
- **App Services (PaaS)** – Managed hosting for web apps, APIs, and backends.  
- **Container Services** –  
  - Azure Container Instances – Quick single container.  
  - Azure Container Apps – Container hosting with scaling.  
  - AKS – Managed Kubernetes.  
- **Azure Virtual Desktop** – Cloud-hosted Windows desktops.  
- **Azure Functions** – Serverless code execution on demand.  
- **VNets** – Private Azure networks with subnets.  
- **NSG** – Firewall rules for subnets/VMs.  
- **VNet Peering** – Connect VNets for cross-network communication.  
- **Azure DNS** – Domain hosting in Azure.  
- **Azure VPN** – Secure device-to-VNet connection.  
- **Site-to-Site VPN** – Connects on-premises network to Azure over internet.  
- **ExpressRoute** – Private, high-speed Azure connection.  

## 5. Azure Storage
- **Azure Storage Account** – Files, blobs, queues, tables; up to 5M GB; ~$0.02/GB/month.  
- **Data Lake** – Large-scale storage for big data analytics.  
- **Blob Storage Redundancy**:  
  - LRS – 3 copies, 1 DC.  
  - ZRS – 3 copies across AZs in a region.  
  - GRS – 3 copies local + 3 in another region.  
  - GZRS – Zone-redundant local + 3 in another region.  
- **Access Tiers** – Hot, Cool, Cold, Archive (trade-off between storage and access cost).  
- **AZCopy** – CLI for fast data transfer to/from Azure Storage.  
- **Storage Explorer** – GUI for accessing Azure storage.  
- **File Storage** – Hierarchical file system.  
- **Azure File Sync** – Sync between on-prem Windows servers and Azure file share.  
- **Azure Migrate** – Assess, plan, and move workloads to Azure.  
- **Azure Data Box** – Offline bulk data transfer (8 TB to 1 PB).  

## 6. Identity, Access & Security
- **Azure AD / Microsoft Entra ID** – Identity and access management.  
- **Conditional Access** – Apply policies based on user, device, location.  
- **Passwordless Auth** – Use biometrics, security keys, or codes instead of passwords.  
- **RBAC** – Assign roles at various scopes: Reader, Contributor, Owner.  
- **Zero Trust Model** – Verify explicitly, least privilege, assume breach.  
- **Microsoft Defender for Cloud** – Security recommendations and threat protection.  
- **Azure Firewall** – Managed, cloud-based network firewall.  
- **NSG** – Traffic control for subnets/VMs.  
- **Application Security Groups** – Group VMs for simplified NSG rules.  

## 7. Cost Management
- **Cost Factors** – Resource type, usage model, service tier, licensing, data transfer, idle resource charges.  
- **Pricing Models** – Pay-as-you-go, reserved (1–3 years), spot instances.  
- **Licensing** – Azure Hybrid Benefit for existing licenses.  
- **Bandwidth** – Inbound free, outbound and inter-region charged.  
- **Tools**:  
  - Azure Pricing Calculator – Estimate costs.  
  - TCO Calculator – Compare on-prem vs. Azure.  
  - Azure Budgets – Track and limit spending.  
  - Resource Tags – Label resources for cost tracking.  

## 8. Governance & Compliance
- **Azure Policy** – JSON rules to enforce compliance (e.g., allowed regions).  
- **Resource Locks** – Prevent deletion/modification (`ReadOnly` or `CannotDelete`).  
- **Microsoft Purview** – Data classification, protection, and compliance monitoring.  

## 9. Management & Deployment Tools
- **Azure Cloud Shell** – Browser-based Bash/PowerShell terminal.  
- **Azure Arc** – Manage non-Azure resources with Azure tools.  
- **ARM Templates** – JSON Infrastructure as Code for resource deployment.  

## 10. Monitoring Tools
- **Azure Advisor** – Cost, security, performance recommendations.  
- **Azure Service Health** – Service outage and issue alerts.  
- **Azure Monitor** – Centralized performance and health dashboard.  
- **Azure Monitor Reports** – Detailed usage and performance analytics.  
