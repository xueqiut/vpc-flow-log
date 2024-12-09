https://catalog.workshops.aws/well-architected-security/en-US/3-detection/40-vpc-flow-logs-analysis-dashboard

Sample VPC
* including Public Subnet, Private Subnet, Internet Gateway, NAT Gateway
* Default Route Table to enable internal VPC routing
* Public Route Table to route traffic to public internet
* Private Route Table to connect instances in private subnet to NAT
* HA in multi-AZs

Sample Web App
* Python
* Run on EC2 instances
* HA in multi-AZs
* Autoscaling with ASG, registered to Target Group
* Automatically launch and deploy through EC2 Template by ASG
* Behind ALB
* Use DynamoDB as backend

VPC Flow Log
* Enabled at VPC level
* Send Log to S3 bucket
* Partitioned by AWS Account, Region, Date...
* Query by Athena
* Metadata (DB, table) created through Glue Catalog
* Table View created by Lambda
* New Partition created by Lambda daily