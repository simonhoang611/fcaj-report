---
title: "Week 2 Worklog"
date: 2026-09-14
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Learn hybrid connectivity between on-premises and AWS: Hybrid DNS, Route 53 Resolver, VM Import/Export.
* Automate operations with Lambda and AWS Systems Manager; build infrastructure as code with CloudFormation and CDK.
* Cost management and network security: limit resources with IAM, Data Lifecycle Manager, VPC Endpoints, AWS WAF.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                                                                                                                                            | Start Date | Completion Date | Reference Material                                                  |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------- |
| 2   | - Learn Hybrid DNS, Route 53 Resolver and VM Import/Export <br> - **Practice:** <br>&emsp; + Connect to a Remote Desktop Gateway (RDGW) over RDP <br>&emsp; + Simulate on-premises DNS with AWS Directory Service; configure DNS <br>&emsp; + Import a virtual machine into AWS; export virtual machines from on-premises and from an EC2 instance                                                              | 21/09/2026 | 21/09/2026      | <https://000010.awsfcaj.com/> <br> <https://000014.awsfcaj.com/>    |
| 3   | - Learn AWS Lambda and AWS Systems Manager <br> - **Practice:** <br>&emsp; + Write code and configure Lambda to automate tasks <br>&emsp; + Use Systems Manager to manage Windows instances                                                                                                                                                                                                                     | 22/09/2026 | 22/09/2026      | <https://000022.awsfcaj.com/> <br> <https://000031.awsfcaj.com/>    |
| 4   | - Learn CloudFormation and advanced CDK <br> - **Practice:** <br>&emsp; + Use basic and advanced CloudFormation to reference resources across stacks <br>&emsp; + Use CDK to build an architecture with API Gateway, Elastic Load Balancer, ECS and Lambda; use nested stacks                                                                                                                                   | 23/09/2026 | 23/09/2026      | <https://000037.awsfcaj.com/> <br> <https://000076.awsfcaj.com/>    |
| 5   | - Learn Infrastructure as Code and EC2 resource optimisation <br> - **Practice:** create a Lambda function and deploy a Three-Tier Architecture                                                                                                                                                                                                                                                                 | 24/09/2026 | 24/09/2026      | <https://000102.awsfcaj.com/> <br> <https://000032.awsfcaj.com/>    |
| 6   | - Learn cost management and resource usage control with IAM and Amazon Data Lifecycle Manager <br> - **Practice:** <br>&emsp; + Create policies limiting service usage by Region, EC2 family, instance size and EBS volume <br>&emsp; + View snapshots managed by Data Lifecycle Manager in the EC2 console <br>&emsp; + Create a policy that automatically creates and retains snapshots on multiple schedules | 25/09/2026 | 25/09/2026      | <https://000064.awsfcaj.com/> <br> <https://000088.awsfcaj.com/vi/> |
| 7   | - Learn VPC Endpoints and AWS Web Application Firewall (WAF) <br> - **Practice:** <br>&emsp; + Use VPC Endpoints so workloads reach AWS services without going over the public Internet <br>&emsp; + Create custom WAF rules to block or allow incoming HTTP requests <br> - Attend the Kickoff FCAJ Buildrathon 2026 and Talkshow “The Thinking Behind Building The Bot” event                                 | 26/09/2026 | 26/09/2026      | <https://000111.awsfcaj.com/> <br> <https://000026.awsfcaj.com/>    |


### Week 2 Achievements:

* Understood how to connect on-premises networks with AWS:
  * Hybrid DNS with Route 53 Resolver
  * Server access through a Remote Desktop Gateway (RDP)
  * Moving virtual machines with VM Import/Export

* Automated operations:
  * Wrote Lambda functions to automate tasks
  * Managed Windows instances with Systems Manager

* Built infrastructure as code:
  * Referenced resources across CloudFormation stacks
  * CDK with nested stacks for API Gateway, ELB, ECS, Lambda
  * Deployed a three-tier architecture

* Cost control:
  * IAM policies limiting Region, EC2 family, instance size, EBS volume
  * Data Lifecycle Manager creating and retaining snapshots on a schedule

* Network security:
  * VPC Endpoints to reach AWS services without the Internet
  * Custom WAF rules to block or allow HTTP requests

* Attended the Kickoff FCAJ Buildrathon 2026 and Talkshow “The Thinking Behind Building The Bot” event on 26/09, the kickoff of the FCAJ Buildrathon.
