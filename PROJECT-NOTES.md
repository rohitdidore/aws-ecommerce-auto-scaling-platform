# Project Notes

## Region
us-east-1 (US East - N. Virginia)

## High-Level Architecture
Internet → Application Load Balancer → Target Group → EC2 Auto Scaling Group → RDS MySQL

## Compute
Two application EC2 instances are maintained across two Availability Zones by the Auto Scaling Group.

## Database
Amazon RDS MySQL is deployed using a DB subnet group for private database networking.

## Web Server
Nginx serves the application page from the EC2 instances.

## Validation
- Auto Scaling Group Instance Refresh completed successfully.
- Target Group reported both instances as Healthy.
- Application was successfully opened through the ALB DNS name.
