# nano-aca-02

Project 2 in the Udacity AWS Cloud Architect nanodegree

Plan, design, provision, and monitor infrastructure in AWS using industry-standard and open source tools. Practice the skills you have learned throughout the course to optimize infrastructure for cost and performance. Use Terraform to provision and configure AWS services in a global configuration.

Project files from [here](https://github.com/maweeks/cand-c2-project).

[First estimate](https://calculator.aws/#/estimate?id=e17cb8f715b5ccfdaa1a3d1d63fd8a37aafa7db8)

[Reduced estimate](https://calculator.aws/#/estimate?id=847253da43ac2233538e37be215af6d3581ba615)

[Increased estimate](https://calculator.aws/#/estimate?id=d20518a3dea86a9f4ce5576e4813cb7086e1ed55)

## Reduced costs changes

- Use more smaller EC2 instances
- Use smaller RDS instances
- Use reserved instances booked in for a year (without paying up front)

## Increased costs changes

- Larger RDS instances
- More EC2 instances for scaling
- Third availability zone set up in us-east-2
  - VPC NAT Gateway
  - CloudFront
  - S3 Bucket
  - Elastic Load Balancing
  - EC2 Auto Scaling (web and application server)
  - RDS read replica

## Need

- Terraform_1_1
- Terraform_1_2

- Terraform_2_1
- Terraform_2_2
- Terraform_2_3

- Terraform_destroyed
