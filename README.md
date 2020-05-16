# nano-aca-02

Project 2 in the Udacity AWS Cloud Architect nanodegree

Plan, design, provision, and monitor infrastructure in AWS using industry-standard and open source tools. Practice the skills you have learned throughout the course to optimize infrastructure for cost and performance. Use Terraform to provision and configure AWS services in a global configuration.

Project files from [here](https://github.com/maweeks/cand-c2-project).

## Budget estimates

[First estimate](https://calculator.aws/#/estimate?id=e17cb8f715b5ccfdaa1a3d1d63fd8a37aafa7db8)

[Reduced estimate](https://calculator.aws/#/estimate?id=847253da43ac2233538e37be215af6d3581ba615)

[Increased estimate](https://calculator.aws/#/estimate?id=d20518a3dea86a9f4ce5576e4813cb7086e1ed55)

### Reduced costs changes

Changes:

- Use more smaller EC2 instances
- Use smaller RDS instances
- Use reserved instances booked in for a year (without paying up front)

Reasoning:

- Using reserved instances will significantly reduce costs but will lock the platform into using the selected infrastructure for the next year. This shouldn't be an issue but would either limit re-architecting the application or waste money.
- Using smaller EC2 instances allows for more granular autoscaling though could reduce performance.
- Using smaller RDS instances allows for significant cost saving but would reduce database performance.

### Increased costs changes

Changes:

- Larger RDS instances
- More EC2 instances for scaling
- Third availability zone set up in us-east-2
  - VPC NAT Gateway
  - CloudFront
  - S3 Bucket
  - Elastic Load Balancing
  - EC2 Auto Scaling (web and application server)
  - RDS read replica

Reasoning:

- Third availability zone in a second region allows for failover if the whole of the `us-east-1` region goes down. This is unlikely to happen but could be worthwhile were something to happen.
- Larger RDS instances improve database performance and prepare for growth of the platform over time.
- More EC2 instances improve application performance and prepare for growth of the platform over time.
