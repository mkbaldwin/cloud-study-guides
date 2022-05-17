# AWS File Storage Services

## Simple Storage Service (S3)

Amazon S3 is a highly scalable object storage service. S3 provides multiple storage classes and pricing options, livecycle management, and security rules.

### Core Concepts

 * **Buckets** - Information in AWS is organized into "buckets". Each bucket has a name that must be:
   * Between 3 and 63 characters long
   * Consist of lowercase letters, numbers, periods (.), underscores (_), and dashes (-)
   * Begin / end with a letter or number
   * Not be formatted as an IP address
   * Names must be unique withing a partition (grouping of regions)
 * **Objects** - Files that are stored in S3 are called objects and are stored in buckets. Each object has a key that is a unique identifier within the bucket. Objects can be up to 5TB in size, but you can only upload files up to 5GB in size at one time.

### Storage Classes

 * **S3 Standard** - Designed to support frequently accessed data, and is replicated across multiple availability zones. No fees for access. 
 * **S3 Standard-IA** - Long-lived, but infrequent access. Retrieval fees apply per GB. Replicated acros multiple availability zones.
 * **S3 One Zone-IA** - Long-lives, infrequently accessed data that is non-critical. 
 * **S3 Intelligent Tiering** - Used for long-lived data with changing or unknown access patterns. Uses historical patterns to determine the appropriate storage class for objects. Monitoring and automation fees per object apply.
 * **S3 Glacier** -  Designed for archival data where access is required within minutes. Must be stored for a minimum of 90 days, can be accessed in as little as 1-5 minutes. Retrieval fees apply per GB.
 * **S3 Glacier Deep Archive** - Used to archive data that is rarely accessed. Must be stored for a minimum of 180 days and can take up to 12 hours to retrieve. Minimum charge will be for the 180 days. Retrieval fees apply per GB. Lowest storage cost in AWS.

### Other Features

 * **Lifecycle Transitions** - Lifecycle transitions can be used to control how objects automatically move between storage classes.
 * **Versioning** - When versioning is enabled for a bucket every copy of a object written to the bucket is kept and assigned a version ID. When deleting an object the data will remain, but a delete marker will be applied.
 * **MFA Delete** - An optional layer of security that requires additional authentication before permanently deleting an object or modifying the version state of the bucket.