# Cloud Concepts

Cloud computing is a term used to describe on-demand access to computing services. Currently, AWS is the largest cloud computing provider. According to Amazon there are six advantages to cloud computing:

  1. **Trade fixed expense for variable expense** - Pay as you go pricing in the cloud allows you to pay only for the resources you use and eliminates the need for large up-front infrastructure investments.
  2. **Benefit from economies of scale** - You can achieve a lower cost with cloud resources than you could do on your own. Because AWS is managing resources for thousands of users you benefit from economies of scale.
  3. **Stop guessing capacity** - Eliminate the need to guess about infrastructure capacity needs. Systems deployed into AWS can scale up or down as needed with minimal notice time.
  4. **Increase speed and agility** - In the cloud new resources are available quickly with a few clicks. This improves organizational agility by getting resources to developers much more quickly. 
  5. **Stop spending money running and maintaining data centers** - With cloud computing there is no data center to maintain and operate. This results in cost savings and allows you to focus on the business and not infrastructure.
  6. **Go global in minutes** - With cloud computing you have access to compute resources world wide with just a few minutes.

Some of the advantages to cloud computing include:

  * **Elasticity** - Ability to acquire resources when needed and release them when no longer needed.
  * **Reliability** - A solution's ability to provude its intended functionality when needed. 
  * **Agility** - Lowers cost of trying new things; less time maintaining infrastructure; access to emerging technologies; reduced risk around security and compliance.

## Cloud Computing Models

  * **Infrastructure as a Service (IaaS)** - This model gives the greatest amount of flexibility and control. IaaS services are very similar to working with your own physical infrastructure, but you are working with virtualized infrastcture components without access to the underlying hardware. 
  * **Platform as a Service (PaaS)** - This model is designed to remove the burden of managing infrastructure resources such as compute, storage, etc. This service offers a platform onto which you deploy your software applications. 
  * **Software as a Service (SaaS)** - With this model applications are fully hosted and managed by the provider. These services take away the need to manage any infrastructure or software. 

## Cloud Deployment Models

 * **Public Cloud** - Deployment onto a public cloud provider like AWS, Azure, or GCP.
 * **Private Cloud (on-premises)** - Deployment onto a cloud-like plaform in your own data center. 
 * **Hybrid** - Applications deployed in an environment that is a mixture of both public and private cloud components. 

## AWS Global Infrastructure

 * **AWS Region** - A cluster of data centers in a specific geographic location working together and providing cloud services.
 * **Availability Zone** - One or more data centers within a specific AWS Region with redundant power, networking, and connectivity. Each region will have multiple availability zones.
 * **AWS Edge Locations** - Data center locations used as a part of a global content delivery network (CDN). These locations only apply to global services such as CloudFront (CDN) and Route 53 (DNS).

## Cloud Economics

Traditional data centers have a very large capital (up-front) expense to get started, plus operational costs for the lifetime of the data center. Additional costs are incurred anytime increased capacity is needed. Cloud on the other hand does not have any up-front expenses. Operational expenses will scale based on your demand/usage (i.e. pay as you go). Traditional data centers also have the potential for unused capacity or unmet demand.

To help manage and predict costs of operating in the cloud AWS provides several tools:

 * **Cost Explorer** - Cost Explorer is a user interface for exploring your costs on AWS. This service allows for cost breakdowns based on service or cost tag. Provides predictions for the next three months of cost based on previous usage, and recommendations for cost optimization.
 * **Budgets** - Allows for planning and tracking usage across AWS services. Supports setting alerts based on different spend criteria. 
 * **TCO Calculator** - Enables determination of costs for leveraging cloud infrastructure. 
 * **Simple Monthly Calculator** - Calculate costs of running specific AWS services/infrastructure.
 * **Organizations** - Allows for managing multiple accounts under a single master account with consolidated billing and clean separation of costs between organizations. Also, provides for centralized logging and security standards.
 * **Resource Tags** -  Metadata that can be attached to specific resources. These are stored as key/value pairs and can be used to identify department, environment, project, etc.

## AWS Support Options

AWS offers different paid support plans based on communication methods, response time, cost, and type of guidance offered. 


|                                          | **Basic** | **Developer**         | **Business**      | **Enterprise**      |
| ---------------------------------------- | :-------: | :-------------------: | :---------------: | :-----------------: |
| Cost                                     | Included  | Starts at $29/mo      | Starts at $100/mo | Starts at $15,00/mo |
| Target Audience                          |           | Individual Developers |                   |                     |
| Documentation, forums, etc.              | 24x7      | 24x7                  | 24x7              | 24x7                |
| Trusted Advisor (7 Checks)               | X         | X                     |                   |                     |
| Trusted Advisor (All Checks)             |           |                       | X                 | X                   |
| Personal Health Dashboard                | X         | X                     | X                 | X                   |
| Business hours email support             |           | X                     | X                 | X                   |
| Designated Contacts                      |           | 1                     | Unlimited         | Unlimited           |
| Dedicated Account Manager                |           |                       |                   | X                   |
| General Guidance Response Time           |           | 24 business hour      | 24 business hour  | 24 business hour    |
| System Impaired Response Time            |           | 12 business hour      | 12 business hour  | 12 business hour    |
| Production System Impaired Response Time |           |                       | 4 hour            | 4 hour              |
| Production System Down Response time     |           |                       | 1 hour            | 1 hour              |
| Business System Down Response Time       |           |                       |                   | 15 minute           |



 * **** - 