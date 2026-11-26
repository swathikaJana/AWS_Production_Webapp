# AWS_Production_Webapp
Hands-on AWS production-style web application project demonstrating EC2 deployment, S3 static website hosting, secure VPC networking with public and private subnets, Internet Gateway, NAT Gateway, Security Groups, Application Load Balancer, Auto Scaling Groups, and multi-AZ high availability.
## AWS Architecture

The project uses a custom AWS VPC across two Availability Zones to demonstrate a highly available web application deployment.

### Architecture Components

- **VPC:** Provides an isolated AWS network.
- **Public Subnets:** Host the Application Load Balancer.
- **Private Subnets:** Host EC2 application instances.
- **Internet Gateway:** Provides internet connectivity.
- **NAT Gateway:** Enables outbound internet access from private instances.
- **Security Groups:** Control inbound and outbound traffic.
- **Application Load Balancer:** Distributes incoming requests across EC2 instances.
- **Auto Scaling Group:** Maintains application instance capacity across Availability Zones.
- **Amazon S3:** Stores static website files and application deployment packages.

### High Availability

The application is deployed across two Availability Zones. If an EC2 instance becomes unhealthy, the Application Load Balancer routes traffic to healthy instances, while the Auto Scaling Group attempts to replace the failed instance.
