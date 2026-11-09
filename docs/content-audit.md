# Content audit — 2026-11-09

Scope: checked all 38 recommended/supporting public resource routes, inspected relevant publisher/GitHub descriptions, compared all 14 official task statements and 119 listed service entries with local reference mentions, and reviewed active notes for high-impact outdated claims. An independent reviewer checked security/network/database/serverless findings. This was not a full transcription of every video, PDF, gated lesson or question bank, nor a guarantee that every old note sentence is correct.

## Corrected notes

- [[03-Storage/01-S3]] — Corrected strong consistency, conditional writes, version IDs and cross-account access evaluation. Sources are attached to the corrected note.
- [[02-Compute-EC2/03-EC2-Instance-Storage]] — Corrected launch-time encryption and instance-store root location; updated regional gp3 limits with Outposts caveat. Sources are attached to the corrected note.
- [[02-Compute-EC2/02-EC2-Associate]] — Corrected placement-group changes for existing stopped instances. Sources are attached to the corrected note.
- [[02-Compute-EC2/01-EC2-Basics]] — Distinguished Compute versus EC2 Instance Savings Plans and corrected the Spot auction/availability analogy. Sources are attached to the corrected note.
- [[02-Compute-EC2/04-High-Availability-Scalability]] — Corrected cooldown behavior and separated it from instance warmup. Sources are attached to the corrected note.
- [[03-Storage/03-S3-Security]] — Corrected Object Lock setup for existing buckets. Sources are attached to the corrected note.
- [[04-Databases/01-RDS-Aurora-ElastiCache]] — Distinguished RDS Multi-AZ deployment types, reconnection needs and Aurora shared storage; marked v1 historical. Sources are attached to the corrected note.
- [[05-Networking-Content-Delivery/02-VPC]] — Corrected CIDR restrictions, IPv6-only subnets and S3 gateway endpoint costs. Sources are attached to the corrected note.
- [[05-Networking-Content-Delivery/03-CloudFront-Global-Accelerator]] — Corrected Global Accelerator no-cache behavior, retired RTMP distributions and OAC/OAI distinction. Sources are attached to the corrected note.
- [[06-Containers-Serverless/01-Containers]] — Added ECS managed EBS support and qualified Fargate storage by orchestrator. Sources are attached to the corrected note.
- [[06-Containers-Serverless/02-Serverless-Overview]] — Corrected DAX query caching and differentiated global-table MREC versus MRSC replication. Sources are attached to the corrected note.
- [[07-Integration-Messaging/01-SQS-SNS-Kinesis]] — Replaced retired Kinesis Data Analytics SQL guidance with current stream-processing distinctions. Sources are attached to the corrected note.
- [[08-Security-Identity/02-Security-Encryption]] — Corrected security group attachment scope and imported KMS key types/on-demand rotation. Sources are attached to the corrected note.
- [[11-Architecture-Patterns/03-Disaster-Recovery-Migrations]] — Qualified Vault Lock guarantees by mode/grace period, Aurora Global Database write topology and DMS compute options. Sources are attached to the corrected note.
- [[11-Architecture-Patterns/05-White-Papers-Architectures]] — Corrected the no-trade-offs claim and removed obsolete support-plan entitlement assumptions. Sources are attached to the corrected note.
- [[10-Machine-Learning/01-ML-Services]] — Corrected Translate feature restrictions, Comprehend input and custom-model claims; labeled Personalize out of scope. Sources are attached to the corrected note.

- [[03-Storage/03-S3-Security]] — additionally corrected default-encryption headers and added DSSE-KMS.
- [[04-Databases/02-Databases-Overview]] — marked QLDB retired and removed it as a current answer shortcut; renamed Flink references.
- [[11-Architecture-Patterns/04-Other-Services]] — added Serverless Application Repository and Wavelength, which lacked active mentions.
- [[12-Exam-Prep/01-Exam-Tips]] — replaced blanket old ID/proctoring rules with official policy links; corrected percentage/scaled-score and practice-test distinctions.
- [[aws-saa-c03-codex-study-guide]] — replaced unchecked experience assumptions and resource/availability claims; original preserved separately.

Active SAA notes no longer carry a Cloud Practitioner tag inherited from the old course. Topic folders and original PDFs/XMind files are preserved. Legacy source dates remain provenance, not evidence of this audit checking every claim. Added an original comparison sheet, design exercises and task/reference map; no quiz attempts, review outcomes, mastery or lab completion were invented.

Independent final review also removed conflicting generic standby/free-tier claims, corrected the DMS body to match its Serverless summary, qualified Memcached availability by deployment type, and removed a false security exemption. Source download metadata (`*:Zone.Identifier`) and local credential files are excluded from the fresh repository index; supplied study assets are preserved.

## Resource-level defects

apgosar's README has the wrong exam fee and domain weights and links to missing files. The checked Jayendra page claims an uncorroborated exam revision. Both are excluded from the core path. Some suggested routes returned 404 and were replaced; JS/gated content and Amazon book metadata remain limited. Cantrill assets and the supplied mind maps are older supporting material. Exact audit decisions and transport evidence are in [[00-Index/Resource-Audit]].

## Remaining limits

Official service availability can diverge from static exam examples; inspect current lifecycle and service-specific docs before deployments. Remaining legacy quota/pricing/marketing details are not all verified; explain the distinction and research them when teaching. Existing source PDFs were preserved, not rewritten. No paid enrollment or cloud deployment occurred. No student knowledge was assessed. Repository publication is authorized for this audit only and must be to the private SAA destination.
