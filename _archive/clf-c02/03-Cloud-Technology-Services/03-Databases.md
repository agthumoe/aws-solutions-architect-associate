---
tags:
  - aws
  - cloud-practitioner
  - technology
  - databases
  - rds
  - dynamodb
domain: Cloud Technology and Services
aliases:
  - "RDS"
  - "Aurora"
  - "DynamoDB"
  - "ElastiCache"
  - "Redshift"
  - "Athena"
  - "Databases"
  - "NoSQL"
status: not-started
date: 2026-07-01
---

# Databases & Analytics

## When to Use a Database vs S3/File Storage

- Use databases when you need to **structure data**, build **indexes** for querying, and define **relationships** between datasets
- Storage (EFS, EBS, S3) has limits — databases are optimized for specific use cases

---

## Relational Databases (SQL)

- Look like Excel spreadsheets with links between tables
- Use SQL to query data
- Best for: structured data with defined relationships

### Amazon RDS (Relational Database Service)

- Managed relational database — **you cannot SSH** into the underlying instance
- Supported engines: **PostgreSQL, MySQL, MariaDB, Oracle, SQL Server, IBM DB2**
- AWS handles: provisioning, patching, backups, monitoring
- Supports automated backups and Multi-AZ deployments

### Amazon Aurora

- AWS proprietary database engine (not open-source)
- Compatible with **MySQL and PostgreSQL**
- **5× faster than MySQL**, **3× faster than PostgreSQL**
- Storage auto-grows in 10 GB increments; up to 128 TB
- ~**20% more expensive** than standard RDS engines
- Highly available by default

### RDS Deployment Options

| Option | Purpose | Notes |
|---|---|---|
| **Read Replicas** | Scale read workloads | Up to 15 replicas; data written to main DB only; replication is **async** |
| **Multi-AZ** | High availability / failover | 1 standby AZ; standby is **passive** (cannot read); automatic failover; replication is **sync** |
| **Multi-Region** | Disaster recovery + local performance | Active in each region; cross-region replication |

### RTO and RPO
| Term | Meaning | RDS Behavior |
|---|---|---|
| **RTO** (Recovery Time Objective) | How quickly must the system recover after an outage | RDS Multi-AZ failover: ~2 minutes |
| **RPO** (Recovery Point Objective) | How much data loss is acceptable | RDS: very low (sync replication means near-zero data loss) |

### Aurora Deployment Details
- **Up to 15 Aurora Replicas** (vs 5 for standard RDS)
- Replication lag: typically **< 10 ms** after primary writes
- Failover timing:
  - To existing Aurora Replica: **~30 seconds**
  - No replicas (recreating primary): **~10 minutes**
- Storage spans **3 AZs** automatically (cluster volume; no copying needed for replicas)
- **URL stays the same** during automatic failover (DNS endpoint)

---

## NoSQL Databases

- Not relational; purpose-built for specific data models
- Flexible schemas
- Benefits: flexibility, scalability (scale-out), high performance

### Amazon DynamoDB

- **Fully managed, serverless NoSQL** database
- Key-value and document data model
- Single-digit millisecond latency at any scale
- Scales to millions of requests per second; trillions of rows; 100s of TB
- Multi-AZ by default; highly available

#### DynamoDB Key Concepts
| Concept | Description |
|---|---|
| **Partition Key** | Required; determines physical storage location (via hash function); must be unique per item if used alone |
| **Sort Key** | Optional; combined with partition key as a **composite primary key**; enables sorting and one-to-many relationships |
| **Composite Key** | Partition Key + Sort Key; items share a partition key but have unique sort keys |
| **Secondary Index** | Alternate key for querying; avoids full table scans; either GSI (Global) or LSI (Local) |

> [!tip]
> "A company needs to query DynamoDB efficiently on a non-primary key attribute" → add a **Secondary Index**.

**DynamoDB Accelerator (DAX)**
- In-memory cache specifically for DynamoDB
- 10× performance improvement; microsecond latency
- No application code changes required

**DynamoDB Global Tables**
- Active-active multi-region replication
- Low-latency access in multiple regions; high availability

> [!tip]
> DynamoDB = serverless NoSQL; great for mobile/gaming/IoT/user profiles. When you see "serverless + NoSQL + low latency" → DynamoDB.

---

## Data Warehousing

### Amazon Redshift

- Based on PostgreSQL but for **OLAP** (Online Analytical Processing)
- Designed for analytics and business intelligence (BI)
- **Columnar** storage (not row-based like traditional databases)
- Massive Parallel Query Execution (MPP)
- Pay per query or per provisioned cluster
- **Serverless option** available

### Amazon Athena

- **Serverless SQL** query service to analyze data in **Amazon S3**
- No infrastructure to manage; pay per query ($5 per TB scanned)
- Built on Presto; supports CSV, JSON, ORC, Avro, Parquet
- Use cases: logs analysis, ad-hoc queries on S3 data

### Amazon QuickSight

- **Serverless, ML-powered Business Intelligence** service
- Create interactive dashboards and visualizations
- Pay per session/user
- Integrates with RDS, Redshift, Athena, S3, and more

---

## Caching

### Amazon ElastiCache

- Managed **Redis or Memcached** in-memory cache
- Reduces load on databases by caching frequently accessed data
- Sub-millisecond latency
- AWS manages OS maintenance, patching, backups, monitoring

---

## Specialized Databases

| Service | Type | Use Case |
|---|---|---|
| **DocumentDB** | NoSQL (document) | AWS-managed MongoDB; JSON documents |
| **Amazon Neptune** | Graph database | Social networks, fraud detection, knowledge graphs |
| **Amazon Timestream** | Time series | IoT, operational applications; time-stamped data |
| **Amazon QLDB** | Ledger database | Financial transactions; immutable; centralized; cryptographically verifiable |
| **Amazon Managed Blockchain** | Blockchain | Decentralized ledger; Hyperledger Fabric & Ethereum |

---

## Data Integration & Migration

### AWS Glue

- **Managed serverless ETL** (Extract, Transform, Load) service
- Prepare and transform data for analytics
- Glue Data Catalog: central metadata repository

### AWS DMS (Database Migration Service)

- Migrate databases to AWS quickly and securely
- Source database remains **available during migration**
- Supports: homogeneous (Oracle→Oracle) and heterogeneous (Oracle→Aurora) migrations

### Amazon EMR (Elastic MapReduce)

- Create **Hadoop clusters** for processing vast amounts of data
- Used for: big data analysis, ML, web indexing
- Supports: Spark, HBase, Presto, Flink

---

## Database Summary Table

| Service | Type | Key Fact |
|---|---|---|
| RDS | Relational SQL | Managed; 6 engines; no SSH |
| Aurora | Relational SQL | 5× MySQL speed; auto-grows; 20% more expensive |
| DynamoDB | NoSQL key-value | Serverless; single-digit ms; DAX for caching |
| ElastiCache | In-memory cache | Redis/Memcached; reduces DB load |
| Redshift | Data warehouse | OLAP; columnar; BI |
| Athena | Serverless SQL | Query S3 data; pay per query |
| QuickSight | BI dashboards | Serverless; ML-powered |
| DocumentDB | NoSQL document | Managed MongoDB |
| Neptune | Graph | Social networks; relationships |
| QLDB | Ledger | Immutable financial records |
| Glue | ETL | Serverless; prepare data for analytics |
| DMS | DB migration | Source stays available |

---

## Exam Tips

> [!tip]
> - RDS = any relational DB; cannot SSH into; AWS patches OS
> - Aurora = fastest AWS DB engine; 5× MySQL; costlier
> - DynamoDB = NoSQL; serverless; millisecond latency
> - Redshift = data warehouse/analytics (OLAP) — NOT for transactional (OLTP)
> - Athena = serverless SQL on S3 — perfect for log analysis
> - ElastiCache = in-memory caching to reduce DB load

> [!warning]
> "OLTP" (Online Transaction Processing) = RDS/Aurora. "OLAP" (Online Analytical Processing) = Redshift.

## Related Notes
- [[01-EC2-Compute]]
- [[02-Storage-S3-EBS-EFS]]
- [[06-Monitoring-Management]]
