---
tags: [aws, cloud-practitioner, moc, integration, messaging]
domain: Cloud Technology and Services
exam-domains: [2, 3]
status: not-started
date: 2026-07-21
---

# Integration & Messaging — Cluster MOC

## Key Concepts

This cluster covers how decoupled applications communicate asynchronously on AWS — the queue model (SQS), the pub/sub model (SNS), and the real-time streaming model (Kinesis) — plus the managed message broker option (Amazon MQ) for lift-and-shift migrations.

## Notes in This Cluster

1. [[01-SQS-SNS-Kinesis]] — SQS Standard vs FIFO, SQS visibility timeout & long polling, SNS pub/sub & fan-out with SQS, SNS message filtering, Kinesis Data Streams vs Amazon Data Firehose, Amazon MQ.

## AWS Services / Features

| Service | Model | Key Fact |
|---|---|---|
| Amazon SQS | Queue (pull) | Decouples producers/consumers; Standard (unlimited throughput) vs FIFO (ordered, exactly-once) |
| Amazon SNS | Pub/Sub (push) | One topic, many subscribers; fan-out with SQS |
| Kinesis Data Streams | Real-time stream (pull/push) | Producer/consumer code, replay capable, up to 365-day retention |
| Amazon Data Firehose | Real-time stream (managed) | Fully managed load into S3/Redshift/OpenSearch, no replay |
| Amazon MQ | Managed message broker | For MQTT/AMQP/STOMP/OpenWire migrations from on-premises |

## Exam Tips
> [!TIP]
> Decoupling architecture questions (Domain 2, Task 2.1) are a core SAA-C03 pattern — recognize when a scenario needs a queue (SQS), a broadcast (SNS fan-out), or a real-time stream (Kinesis), versus a lift-and-shift broker migration (Amazon MQ).

## Related Notes
- [[01-SQS-SNS-Kinesis]]
