# fargate-cloudformation-example

An example CloudFormation template that deploys a container to AWS Fargate as a service.

Multiple AZs are used for high availability, SSL is terminated at the load balancer, health checks are used, a DNS record is created, and it scales to keep CPU utilization at or below 50%. Specifically, it includes:

* A cluster
* A task definition for the container
* An ECS service
* A load balancer and its associated listener and target group
* The necessary IAM roles
* Logging to CloudWatch Logs, including the creation of a log group
* Security groups for the container and load balancer
* A DNS record for Route 53
* An auto scaling policy