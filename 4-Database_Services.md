# AWS Database Services

## Amazon Relational Database Service (RDS)

Amazon RDS is a fully-managed database service that makes it easy to operate a database in the cloud. RDS has support for multiple database server engines:

  * MySQL / MariaDB
  * PostgreSQL
  * Oracle
  * SQL Server
  * Aurora

Key features of RDS include:
  * Read repliation for improved performance.
  * Multi-AZ deployments for availability.
  * Runs on EC2 instances, but you do not have access to the instances. AWS is fully responsible for the security and management of the datbase server instance.
  * Support for automatic backups. Automatic backups are performed daily and transaction logs are retained throughout the day. This allows for restoration to a very specific time if needed. **These backups are deleted when the RDS instance is deleted.**
  * Support for DB snapshots performed manually by the administrator. These are retained even if the RDS instance is deleted. 

## Aurora

## DynamoDB

## Redshift

## Elasticache