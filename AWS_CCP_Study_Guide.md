---
title: "AWS Cloud Practitioner Study Guide"
date: December 2022
documentclass: report
geometry: "margin=.75in"
linestretch: 1.25
numbersections: true
secnumdepth: 1
output: pdf_document
---

# Fundamental Concepts

## Benefits of Cloud

Six Advantages of Cloud Computing

   1. **Trade fixed expense for variable expense** - Pay as you go pricing in the cloud allows you to pay only for the 
                                                     resources you use and eliminates the need for large up-front 
                                                     infrastructure investments. Trade capital expense (CAPEX) for
                                                     operational expense (OPEX).
   2. **Benefit from economies of scale** - You can achieve a lower cost with cloud resources than you could do on your own. 
                                            Because AWS is managing resources for thousands of users you benefit from 
                                            economies of scale.
   3. **Stop guessing capacity** - Eliminate the need to guess about infrastructure capacity needs. Systems deployed into 
                                   AWS can scale up or down as needed with minimal notice time.
   4. **Increase speed and agility** - In the cloud new resources are available quickly with a few clicks. This improves 
                                       organizational agility by getting resources to developers much more quickly.
   5. **Stop spending money running and maintaining data centers** - With cloud computing there is no data center to maintain 
                                                                     and operate. This results in cost savings and allows you 
                                                                     to focus on the business and not infrastructure.
   6. **Go global in minutes** - With cloud computing you have access to compute resources worldwide with just a few minutes.

Additional advantages of cloud architectures include:

  * **Elasticity** - Ability to acquire resources when needed and release them when no longer needed.
  * **Reliability** - A solution's ability to provide its intended functionality when needed.
  * **Agility** - Lowers cost of trying new things; less time maintaining infrastructure; access to emerging technologies; 
                  reduced risk around security and compliance.

## Cloud Computing Models

  * **Infrastructure as a Service (IaaS)** - This model gives the greatest amount of flexibility and control. IaaS services 
                                             are very similar to working with your own physical infrastructure, but you are
                                             working with virtualized infrastructure components without access to the 
                                             underlying hardware.
  * **Platform as a Service (PaaS)** - This model is designed to remove the burden of managing infrastructure resources 
                                       such as compute, storage, etc. This service offers a platform onto which you 
                                       deploy your software applications.
  * **Software as a Service (SaaS)** - With this model applications are fully hosted and managed by the provider. These 
                                       services take away the need to manage any infrastructure or software.

## Cloud Deployment Models

  * **Public Cloud** - Deployment onto a public cloud provider like AWS, Azure, or GCP.
  * **Private Cloud (on-premises)** - Deployment onto a cloud-like platform in your own data center.
  * **Hybrid** - Applications deployed in an environment that is a mixture of both public and private cloud components.

## AWS Global Infrastructure

  * **AWS Region** - A cluster of data centers in a specific geographic location working together and providing cloud services.
  * **Availability Zone** - One or more data centers within a specific AWS Region with redundant power, networking, and 
                            connectivity. Each region will have multiple availability zones.
  * **AWS Edge Locations** - Data center locations used as a part of a global content delivery network (CDN). These locations 
                             only apply to global services such as CloudFront (CDN) and Route 53 (DNS). 

## Shared Responsibility Model

The **customer** is responsible for security of services running in the cloud. This includes OS level security patches
on EC2, software configuration / patching for custom or third-party software. 

**AWS* is responsible for security of the cloud. This includes the AWS network and server infrastructure, and underlying
operating systems for managed services that do not provide OS level access.

## Cloud Economics

Traditional data centers have a very large capital (up-front) expense to get started, plus operational costs for the 
lifetime of the data center. Additional costs are incurred anytime increased capacity is needed. Cloud on the other 
hand does not have any up-front expenses. Operational expenses will scale based on your demand/usage (i.e. pay as 
you go). Traditional data centers also have the potential for unused capacity or unmet demand.

To help manage and predict costs of operating in the cloud AWS provides several tools:

  * **Cost Explorer** - Cost Explorer is a user interface for exploring your costs on AWS. This service allows for cost 
                        breakdowns based on service or cost tag. Provides predictions for the next three months of cost 
                        based on previous usage, and recommendations for cost optimization.
  * **Budgets** - Allows for planning and tracking usage across AWS services. Supports setting alerts based on different spend criteria.
  * **TCO Calculator** - Enables determination of costs for leveraging cloud infrastructure.
  * **Simple Monthly Calculator** - Calculate costs of running specific AWS services/infrastructure.
  * **Organizations** - Allows for managing multiple accounts under a single master account with consolidated billing and 
                        clean separation of costs between organizations. Also, provides for centralized logging and security standards.
  * **Resource Tags** -  Metadata that can be attached to specific resources. These are stored as key/value pairs and can 
                         be used to identify department, environment, project, etc.

\pagebreak

## AWS Support Options

AWS offers different paid support plans based on communication methods, response time, cost, and type of guidance offered.

|                                  | **Basic** |  **Developer**  |  **Business**  | **Enterprise** |
|----------------------------------|:---------:|:---------------:|:--------------:|:--------------:|
| Starting Cost                    | Included  |     $29/mo      |    $100/mo     |   $15,000/mo   |
| Target Audience                  |           | Individual Devs |                |                |
| Documentation, forums, etc.      |   24x7    |      24x7       |      24x7      |      24x7      |
| Trusted Advisor (7 Checks)       |    Yes    |       Yes       |                |                |
| Trusted Advisor (All Checks)     |           |                 |      Yes       |      Yes       |
| Personal Health Dashboard        |    Yes    |       Yes       |      Yes       |      Yes       |
| Business hours email support     |           |       Yes       |      Yes       |      Yes       |
| Designated Contacts              |           |        1        |   Unlimited    |   Unlimited    |
| Dedicated Account Manager        |           |                 |                |      Yes       |
| General Guidance Response Time   |           | 24 business hr  | 24 business hr | 24 business hr |
| System Impaired Response Time    |           | 12 business hr  | 12 business hr | 12 business hr |
| Prod. Sys Impaired Response Time |           |                 |      4 hr      |      4 hr      |
| Prod. Sys Down Response Time     |           |                 |      1 hr      |      1 hr      |
| Business Sys Down Response Time  |           |                 |                |     15 min     |
Table: Comparison of AWS Support Plans

# Services Overview

## Compute Services
  * **EC2** - Elastic Compute Cloud provides access to on-demand compute resources. EC2 is basically a virtual machine
              running in the cloud on AWS infrastructure.
  * **Elastic Beanstalk** - Automates the deployment and scaling of workloads on EC2 (PaaS). You only pay for other
                            services used and not for elastic beanstalk itself. Works for specific application platforms
                            (Java, .NET, Node, Docker, etc).
  * **AWS Lambda** - Platform for running serverless applications (cloud functions). You pay based on function execution
                     time and memory.

## Content and Network Delivery Services
  * **Amazon Virtual Private Cloud (VPC)** - A VPC is a "container" in which you run all of your services. It is a logically
                                             separated part of AWS for your use and provides virtual networking configurable 
                                             for your application. 
  * **AWS Direct Connect** - Allows for establishing a connection from AWS directly to your data center.
  * **Amazon Route 53** - Global service (no regions) for providing DNS.
  * **Elastic Load Balancing** - Cloud based load balancers to distribute traffic across multiple EC2, ECS, or Lambda
                                 targets. Multiple types of load balancers available: application (ALB), network (NLB),
                                 or classic.
  * **Cloud Front** - Global content delivery network (CDN) utilizing AWS edge locations. Can be used for both static
                      and dynamic content. Includes security features such as DDoS protection and web application firewall (WAF). 
  * **Amazon API Gateway** - Fully managed API service. Integrates with multiple AWS services and provides monitoring 
                             and metrics on API calls.
  * **AWS Global Accelerator** - Routes via AWS global edge locations. Once a request reaches an edge location it is 
                                 routed within AWS network instead of internet. Improves performance and has superior
                                 fault tolerance. 

## File Storage Services
  * **Amazon Simple Storage Service (S3)** - Fully managed file storage service that stores files as objects in buckets.
                                             Storage across multiple AZs with multiple storage classes and lifecycle policies.
  * **Elastic Block Store (EBS)** - Persistent block storage for use on EC2 instances. Allows for redundancy within AZ
                                    and can scale to support petabytes of data.
  * **Elastic File System (EFS)** - Fully managed NFS file system designed for linux workloads. Supports petabyte scale
                                    and storage across multiple AZs.
  * **Amazon FSx** - Fully managed Windows file system with SMB/NTFS support and AD integration.
  * **AWS Snow Ball** - Physical device shipped to your location to move petabyte scale information into S3.
  * **AWS Snow Mobile** - Shipping container brought to your location for moving exabyte scale information into S3.

## Database Services
  * **Amazon Relational Database Service (RDS)** - Fully managed relational database service supporting common database
                                                   engines such as MySQL, PostgreSQL, Oracle, etc.
  * **Amazon Aurora** - MySQL/PostgreSQL compatible database built for the cloud.
  * **Amazon Database Migration Service (DMS)** - Tooling for one time or continual data migration into Amazon RDS from
                                                  many different commercial database systems.
  * **Amazon Dynamo DB** - Fully managed no SQL DB. Support key-value storage or document storage. Has extremely low latency
                           and automatic scaling. Can handle up to 20 millions requests per second.
  * **Amazon ElastiCache** - Fully managed in memory datastore with on demand scaling and replication. Used for caching
                             and session storage. Compatible with redis and memcached. 
  * **Amazon Red Shift** - Data warehouse service supporting high performance and petabyte scale. Uses column oriented storage.

## Integration Services
  * **Simple Notification Service (SNS)** - Publish / subscribe messaging service supporting topics. Supports notifications
                                            via SMS, email, or push.
  * **Simple Queue Service (SQS)** - Message queueing service that supports up to 256k payload. Message can be stored up
                                     to 14 days. Supports standard (order not guaranteed) or FIFO (order guaranteed) queues.
  * **AWS Step Functions** - Serverless tool for orchestration of workflows. Amazon states language (DSL) for defining workflows.

## Management and Governance Services
  * **AWS Cloud Trail** - Logging and monitoring of interactions across all AWS services into S3 buckets. Used for 
                          compliance, forensic analysis, operational analysis, and troubleshooting. 
  * **AWS Cloud Watch** - Logging service for your application and AWS services. Metrics, alarms, and logs for infrastructure. 
  * **AWS Config** - Monitors and records configuration and history of infrastructure. 
  * **AWS Systems Manager** - Set of tools for managing infrastructure. Secure way to access server using AWS credentials.
  * **AWS Cloud Formation** - Automates provisioning of cloud infrastructure by building templates in YAML or JSON. 
  * **AWS OpsWorks** - Managed instances of chef and puppet.
  * **AWS Organizations** - Provides consolidated billing, logging, security, and account management for multiple accounts
                            under a single master account.
  * **AWS Control Tower** - Centralize user access and management across multiple accounts.

## Identity and User Management

  * **AWS Identity and Access Management (IAM)** - Service for defining users and controlling access to AWS services. Performs
                                                   authentication and authorization management (including multi-factor authentication).
  * **Amazon Cognito** - Manage authentication / authorization for your custom applications and provides a fully managed user 
                         directory service. Enabled controlled access to AWS resources (e.g. S3 bucket) and works with enterprise
                         IdPs (e.g. AD, SAML).

## Data Processing Services
  * **AWS Glue** - Serverless extract, transform, and load (ETL) service for RDS, DynamoDB, RedShift, S3. 
  * **Amazon EMR** - Elastic map reduce service for big data processing (includes Spark, Flink, Hive, HBase, Hudi, and Presto support).
  * **AWS Data Pipeline** - Managed extract, transform, and load (ETL) service with data workflows.
  * **Amazon Athena** - Managed service for querying large scale data in S2 using standard SQL style queries.
  * **Amazon Quick Sight** - Managed business intelligence service and dynamic dashboards.
  * **Amazon Cloud Search** - Managed service that enables developers to build search capabilities into custom applications.
  * **Amazon Rekognition** - Computer vision image/video recognition used to identify object, actions, or perform facial recognition. 
  * **Amazon Translate** - Text translation service for 54 different languages.
  * **Amazon Transcribe** - Speech recognition / transcription for 31 different languages.

## Developer Tools

  * **AWS CodeCommit** - Private Git repository hosting on AWS cloud.
  * **AWS CodeBuild** - CI tool that compiles code, runs test, and produces deployable software packages. 
  * **AWS CodePipeline** - Continuous delivery tool for building build/deployment pipelines. 

# Architecture Principles

## Well-Architected Framework

The AWS Well-Architected Framework is designed to help you understand pros and cons to decisions about building 
systems in the cloud.

Six Pillars

  * **Operational Excellence** - This pillar focuses on running and monitoring systems, and continually improving
                               processes/procedures.
  * **Security** - Focus on protecting information and systems. 
  * **Reliability** - Focus on workloads performing their intended functions, and the ability to recover quickly from failures.
  * **Performance Efficiency** - Streamlined allocation of resources. Selecting resource types and sizes optimized for
                               workload requirements. 
  * **Cost Optimization** - Focuses on avoiding unnecessary costs.
  * **Sustainability**  - Focuses on minimizing the environmental impact of running services.

# Compute Services

## Elastic Compute Cloud (EC2)

The Amazon Elastic Compute Cloud (EC2) provides compute resources (e.g. virtual servers) in the cloud. These EC2 
instances are suitable for a wide range of use cases including: web application hosting, batch processing, API servers, 
desktop in the cloud, etc.

Each server created in EC2 (aka Instance) has a defined instance type consisting of processor, memory and storage. 
Instance type cannot be changed without downtime. Instances come in multiple categories: general purpose, compute 
optimized, memory optimized, storage optimized, or accelerated computing.

### EC2 Storage Options

When creating an EC2 instance a root device type must be selected. This determines how the volume used to boot the 
instance will be stored. There are two root device types to choose from.

  * **Instance Store** - Ephemeral storage that is maintained only while the instance is running. At boot the storage 
                         location is created and the image content is copied to the volume.
  * **Elastic Block Store (EBS)** - Provides a persistent volume that is stored separately from the EC2 instance. 
                                    This is the most commonly used storage mechanism for EC2.

### Machine Images

EC2 instances are created based on Amazon Machine Images (AMI). An AMI provides a template for an EC2 instance including 
OS, configuration, and initial data. AWS provides many images to use as a starting point, or you can obtain images from 
a marketplace. Custom AWS images can be made and shared across accounts within an organization.

### Purchase Options

  * **On-demand** - Standard purchase method for EC2 instances. Billed per second while the instance is in the `running` 
                  state. No time based commitment required.
  * **Reserved** - Reserved instances provide significant cost savings over on-demand instances, but they require a 
                   commitment to run the instance for a specific amount of time. This is not a dedicated server.
  * **Savings Plan** - Similar to a reserved instance, but you are making a commitment measured in USD per hour.
  * **Spot** - Significant cost savings for use cases that are flexible about when they are run and if they can be interrupted.
  * **Dedicated** - Most expensive. Good if you have a per server licensing model to adhere to. Some types of compliance models need this.

## Elastic Beanstalk

Amazon Elastic Beanstalk is a service that makes it easier to deploy applications on AWS. Supports specific technologies 
including Java, Node.js, Docker, and more. Leverages other AWS technologies. So, you only pay for the other services 
used and not for elastic beanstalk itself.

Elastic beanstalk allows for deploying applications with minimal knowledge of other AWS services. This is a lower 
maintenance service, but provides less customization options. Features include: monitoring, deployment, and scaling.

## AWS Lambda

AWS Lambda is a serverless computing service that allows for application code to run without provisioning any server 
infrastructure. Commonly referred to as functions as a service. Only pay for what you use based on execution time and 
memory. Integrates well with event driven architectures and other AWS services. Benefits include: low maintenance, 
auto-scaling, fault-tolerance, servers architecture, and pay by usage.

## Elastic Load Balancing

AWS elastic load balancing is a highly available and scalable service for managing traffic into an application. 
The service runs always in at least two availability zones and includes autoscaling based on load.

There are four types of load balancers:

  * **Application Load Balancer (ALB)** - An application load balancer works at the application layer (OSI layer 7) and can 
                                  load balance/proxy HTTP/HTTPS traffic. Allows for specifying advanced routing rules.
  * **Network Load Balancer (NLB) ** - A network load balancer works at the transport layer (OSI layer 4) and is capable of load 
                                balancing most TCP/UDP protocols.
  * **Gateway Load Balancer** - Provides cloud native load balancing for virtual appliances.
  * **Classic Load Balancer** - Older style of load balancer that supports TCP/SSL connections and EC2-classic. Supports 
                                sticky sessions using application-generated cookies.

# Database Services

## Amazon Relational Database Service (RDS)

Amazon RDS is a fully-managed database service that makes it easy to operate a database in the cloud. 
RDS has support for multiple database server engines:

  * MySQL / MariaDB
  * PostgresSQL
  * Oracle
  * SQL Server
  * Aurora

Key features of RDS include:

  * Read replication for improved performance.
  * Multi-AZ deployments for availability.
  * Runs on EC2 instances, but you do not have access to the instances. AWS is fully responsible for the security and 
    management of the database server instance.
  * Support for automatic backups. Automatic backups are performed daily and transaction logs are retained throughout 
    the day. This allows for restoration to a very specific time if needed. **These backups are deleted when the RDS 
    instance is deleted.**
  * Support for DB snapshots performed manually by the administrator. These are retained even if the RDS instance is deleted. 