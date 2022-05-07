# AWS Compute Services

## Elastic Compute Cloud (EC2)

The Amazon Elastic Compute Cloud (EC2) provides compute resources (e.g. virtual servers) in the cloud. These EC2 instances are suitable for a wide range of use cases including: web application hosting, batch processing, API servers, desktop in the cloud, etc. 

Each server created in EC2 (aka Instance) has a defined instance type consisting of processor, memory and storage. Instance type cannot be changed without downtime. Instances come in multiple categories: general purpose, compute optimized, memory optimized, storage optimized, or accelerated computing. 

### Storage 

When creating an EC2 instance a root device type must be selected. This determines how the volume used to boot the instance will be stored. There are two root device types to choose from.

  * **Instance Store** - Ephemeral storage that is only maintained only while the instance is running. At bootup the storage location is created and the image content is copied to the volume.
  * **Elastic Block Store (EBS)** - Provides a persistent volume that is stored separately from the EC2 instance. This is the most commonly used storage mechanism for EC2. 

### Machine Images

EC2 instances are created based on Amazon Machine Images (AMI). An AMI provides a template for an EC2 instance including OS, configuration, and initial data. AWS provides many images to use as a starting point, or you can obtain images from a marketplace. Custom AWS images can be made and shared across accounts within an organization.

### Purchase Options

    * **On-demand** - Standard purchase method for EC2 instances. Billed per second while the instance is in the `running` state. No time based commitment required.
    * **Reserved** - Reserved instances provide significant cost savings over on-demand instances, but they require a commitment to run the instance for a specific amount of time. This is not a dedicated server.
    * **Savings Plan** - Similar to a reserved instance, but you are making a commitment measured in USD per hour.
    * **Spot** - Significant cost savings for use cases that are flexible about when they are run and if they can be interrupted. 
    * **Dedicated** - Most expensive. Good if you have a per server licensing model to adhere to. Some types of compliance models need this.

## Elastic Beanstalk

Amazon Elastic Beanstalk is a service that makes it easier to deploy applications on AWS. Supports specific technologies including Java, Node.js, Docker, and more. Leverages other AWS technologies. So, you only pay for the other services used and not for elastic beanstalk itself. 

Elastic beanstalk allows for deplyoing applications with minimal knowledge of other AWS services. This is a lower maintenance service, but provides less customization options. Features include: monitoring, deployment, and scaling. 

## AWS Lambda

AWS Lambda is a serverless computing service that allows for application code to run without provisioning any server infrastructure. Commonly referred to as functions as a service. Only pay for what you use based on execution time and memory. Integrates well with event driven architectures and other AWS services. Benefits include: low maintenance, auto scaling, fauly tolerence, serveless architecture, and pay by usage.


