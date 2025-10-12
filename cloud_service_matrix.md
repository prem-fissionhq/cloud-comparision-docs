# Cloud Services Comparison Matrix
## AWS vs Azure vs Google Cloud Platform

---

## Use Case 1: 3-Tier Web Application

### Compute Services

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Virtual Machines** | EC2 | Virtual Machines | Compute Engine | Core IaaS compute |
| **VM Pricing Models** | On-Demand, Reserved, Spot | Pay-as-you-go, Reserved, Spot | On-Demand, Committed Use, Preemptible | GCP offers sustained use discounts automatically |
| **Auto Scaling** | Auto Scaling Groups | Virtual Machine Scale Sets | Managed Instance Groups | All support horizontal scaling |
| **Serverless Compute** | Lambda | Azure Functions | Cloud Functions | For backend logic |
| **Container Instances** | ECS Fargate | Container Instances | Cloud Run | Serverless containers |

### Load Balancing & Networking

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Application Load Balancer** | Application LB (ALB) | Application Gateway | HTTP(S) Load Balancer | Layer 7, SSL termination |
| **Network Load Balancer** | Network LB (NLB) | Load Balancer (Standard) | Network Load Balancer | Layer 4, high performance |
| **Global Load Balancing** | Route 53 + CloudFront | Traffic Manager + Front Door | Cloud Load Balancing | GCP has native global LB |
| **Virtual Network** | VPC | Virtual Network (VNet) | VPC | Network isolation |
| **CDN** | CloudFront | Azure CDN / Front Door | Cloud CDN | Content delivery |
| **DNS** | Route 53 | Azure DNS | Cloud DNS | Managed DNS service |
| **Private Connectivity** | Direct Connect | ExpressRoute | Cloud Interconnect | Dedicated connections |

### Storage Services

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Object Storage** | S3 | Blob Storage | Cloud Storage | Static content, backups |
| **Storage Tiers - Hot** | S3 Standard | Hot tier | Standard | Frequent access |
| **Storage Tiers - Cool** | S3 IA, Glacier | Cool, Archive | Nearline, Coldline | Infrequent access |
| **File Storage** | EFS | Azure Files | Filestore | NFS/SMB shares |
| **Block Storage** | EBS | Managed Disks | Persistent Disk | VM attached storage |

### Database Services

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Relational (MySQL)** | RDS for MySQL | Azure Database for MySQL | Cloud SQL for MySQL | Managed MySQL |
| **Relational (PostgreSQL)** | RDS for PostgreSQL | Azure Database for PostgreSQL | Cloud SQL for PostgreSQL | Managed PostgreSQL |
| **Relational (SQL Server)** | RDS for SQL Server | Azure SQL Database | Cloud SQL for SQL Server | Microsoft SQL Server |
| **Enterprise Database** | RDS for Oracle | Oracle on Azure | Oracle on GCP | Licensed databases |
| **Proprietary Database** | Aurora | Azure SQL Database | Cloud Spanner | Cloud-native RDBMS |
| **NoSQL - Document** | DocumentDB | Cosmos DB | Firestore | Document databases |
| **NoSQL - Key-Value** | DynamoDB | Cosmos DB (Table API) | Firestore/Bigtable | High-performance KV store |

### Caching

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **In-Memory Cache** | ElastiCache (Redis) | Azure Cache for Redis | Memorystore for Redis | Redis caching |
| **In-Memory Cache** | ElastiCache (Memcached) | Azure Cache (Memcached) | Memorystore for Memcached | Memcached option |

### Security & Identity

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Identity Management** | IAM | Azure AD / Entra ID | Cloud IAM | User & service identity |
| **Secrets Management** | Secrets Manager | Key Vault | Secret Manager | API keys, passwords |
| **Firewall** | Security Groups, NACL | Network Security Groups | Firewall Rules | Network security |
| **WAF** | AWS WAF | Azure WAF | Cloud Armor | Web application firewall |
| **DDoS Protection** | Shield | DDoS Protection | Cloud Armor | DDoS mitigation |

---

## Use Case 2: Container Orchestration & Microservices

### Container Services

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Managed Kubernetes** | EKS (Elastic Kubernetes Service) | AKS (Azure Kubernetes Service) | GKE (Google Kubernetes Engine) | GKE most mature (Google created K8s) |
| **Container Registry** | ECR (Elastic Container Registry) | ACR (Azure Container Registry) | Artifact Registry / GCR | Private image storage |
| **Container Orchestration** | ECS (Elastic Container Service) | Container Instances | Cloud Run | Proprietary to AWS |
| **Serverless Containers** | Fargate | Container Instances | Cloud Run | No server management |
| **Service Mesh** | App Mesh | Service Mesh (OSM) | Anthos Service Mesh | Traffic management |

### CI/CD & DevOps

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Source Control** | CodeCommit | Azure Repos | Cloud Source Repositories | Git repositories |
| **Build Service** | CodeBuild | Azure Pipelines | Cloud Build | CI/CD pipelines |
| **Deployment** | CodeDeploy | Azure Pipelines | Cloud Deploy | Automated deployment |
| **Pipeline** | CodePipeline | Azure DevOps | Cloud Build + Deploy | End-to-end CI/CD |
| **Artifact Management** | CodeArtifact | Azure Artifacts | Artifact Registry | Package management |

### Monitoring & Logging

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Monitoring** | CloudWatch | Azure Monitor | Cloud Monitoring (Stackdriver) | Metrics & alerts |
| **Logging** | CloudWatch Logs | Azure Monitor Logs | Cloud Logging | Centralized logging |
| **Tracing** | X-Ray | Application Insights | Cloud Trace | Distributed tracing |
| **Debugging** | X-Ray | Application Insights | Cloud Debugger | Production debugging |
| **Profiling** | CodeGuru Profiler | Application Insights Profiler | Cloud Profiler | Performance profiling |

### API Management

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **API Gateway** | API Gateway | API Management | API Gateway / Apigee | REST/HTTP APIs |
| **GraphQL** | AppSync | API Management | Apigee | GraphQL support |

---

## Use Case 3: Data Analytics & Warehouse

### Data Ingestion

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Real-time Streaming** | Kinesis Data Streams | Event Hubs | Pub/Sub | Message streaming |
| **Message Queue** | SQS | Queue Storage / Service Bus | Pub/Sub | Asynchronous messaging |
| **Event Grid** | EventBridge | Event Grid | Eventarc | Event-driven architecture |
| **Data Transfer** | DataSync / Snow Family | Data Box / AzCopy | Transfer Appliance / Service | Bulk data migration |

### Data Processing

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Batch Processing** | EMR (Hadoop/Spark) | HDInsight / Databricks | Dataproc | Big data processing |
| **ETL Service** | Glue | Data Factory | Dataflow | Extract, transform, load |
| **Stream Processing** | Kinesis Data Analytics | Stream Analytics | Dataflow | Real-time processing |
| **Serverless ETL** | Glue | Data Factory | Dataflow | Managed ETL |
| **Workflow Orchestration** | Step Functions / MWAA | Logic Apps / Data Factory | Cloud Composer (Airflow) | Workflow automation |

### Data Warehouse

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Data Warehouse** | Redshift | Synapse Analytics | BigQuery | Petabyte-scale analytics |
| **Architecture** | Cluster-based (provisioned) | Hybrid (provisioned/serverless) | Fully serverless | BigQuery = zero admin |
| **Pricing Model** | Hourly node pricing | DWU or serverless | On-demand or flat-rate | BigQuery charges by query |
| **Data Lake** | S3 + Athena | ADLS Gen2 + Synapse | Cloud Storage + BigQuery | Query data in storage |

### Analytics & BI

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Interactive Query** | Athena | Synapse Serverless SQL | BigQuery | Query without loading |
| **Business Intelligence** | QuickSight | Power BI | Looker / Looker Studio | Visualization & dashboards |
| **Notebook Environment** | SageMaker Notebooks | Azure Notebooks / Synapse | Vertex AI Workbench | Jupyter notebooks |
| **Data Catalog** | Glue Data Catalog | Azure Purview | Data Catalog | Metadata management |

### Machine Learning (Bonus)

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **ML Platform** | SageMaker | Azure Machine Learning | Vertex AI | End-to-end ML |
| **AutoML** | SageMaker Autopilot | Azure AutoML | Vertex AI AutoML | Automated model training |
| **Model Deployment** | SageMaker Endpoints | Azure ML Endpoints | Vertex AI Endpoints | Model serving |
| **Pre-trained Models** | Rekognition, Comprehend | Cognitive Services | Vision AI, Natural Language AI | Ready-to-use AI APIs |
| **MLOps** | SageMaker Pipelines | Azure ML Pipelines | Vertex AI Pipelines | ML workflow automation |

---

## Cross-Cutting Services

### Management & Governance

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Cost Management** | Cost Explorer | Cost Management | Cloud Billing | Cost tracking & optimization |
| **Resource Provisioning** | CloudFormation | ARM Templates / Bicep | Deployment Manager | Infrastructure as Code |
| **Multi-cloud IaC** | Terraform | Terraform | Terraform | Cross-cloud provisioning |
| **Policy & Compliance** | Organizations, Config | Azure Policy | Organization Policy | Governance |
| **Audit Logging** | CloudTrail | Activity Log | Cloud Audit Logs | Compliance tracking |

### Hybrid & Multi-Cloud

| Service Category | AWS | Azure | GCP | Notes |
|-----------------|-----|-------|-----|-------|
| **Hybrid Platform** | Outposts | Azure Stack / Arc | Anthos | On-premises extension |
| **Multi-cloud Management** | - | Azure Arc | Anthos | Manage resources anywhere |

---

## Key Differentiators Summary

### AWS Strengths
- Broadest service portfolio (200+ services)
- Largest market share and ecosystem
- Most third-party integrations
- Strong enterprise support

### Azure Strengths
- Best for Microsoft shops (AD, Office 365, Windows)
- Hybrid cloud leadership (Azure Arc, Stack)
- Strong enterprise compliance
- Integrated with GitHub

### GCP Strengths
- Best-in-class data analytics (BigQuery)
- Kubernetes expertise (created K8s)
- Strong ML/AI capabilities
- Simplest pricing model
- Superior global network infrastructure

---

## Decision Factors

### Choose AWS if:
- Need the widest range of services
- Heavy AWS marketplace usage
- Large existing AWS footprint
- Need mature enterprise features

### Choose Azure if:
- Microsoft-centric organization
- Hybrid cloud requirements
- Enterprise agreements with Microsoft
- Strong Windows workload requirements

### Choose GCP if:
- Data analytics heavy workloads
- Kubernetes-first strategy
- ML/AI innovation priority
- Want simplest pricing and operations
- Need best network performance