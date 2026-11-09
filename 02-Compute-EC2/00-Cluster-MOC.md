---
tags: [aws, saa-c03, moc]
status: not-started
date: 2026-07-21
---

# Compute - EC2

Covers Amazon EC2 fundamentals through advanced configuration, instance storage options (EBS, Instance Store, EFS, AMI), and high-availability/scalability building blocks (Elastic Load Balancers and Auto Scaling Groups). Source: AWS Certified Solutions Architect Slides v48 (Stéphane Maarek), pages 41–159.

## Notes
- [[01-EC2-Basics]] — EC2 fundamentals: sizing, instance type families & naming, security groups, SSH access methods, and an overview of instance purchasing options (On-Demand, Reserved, Savings Plans, Spot, Dedicated Hosts/Instances, Capacity Reservations)
- [[02-EC2-Associate]] — Private/public/Elastic IPs, placement groups (Cluster/Spread/Partition), Elastic Network Interfaces, and EC2 Hibernate
- [[03-EC2-Instance-Storage]] — EBS volumes, snapshots, AMIs, EC2 Instance Store, EBS volume types (gp2/gp3, io1/io2, st1, sc1), EBS encryption, and Amazon EFS
- [[04-High-Availability-Scalability]] — Vertical vs horizontal scaling, Elastic Load Balancer types (CLB, ALB, NLB, GWLB), sticky sessions, cross-zone load balancing, SSL/SNI, and Auto Scaling Groups
