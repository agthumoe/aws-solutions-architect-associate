---
tags:
  - aws
  - cloud-practitioner
  - technology
  - sqs
  - sns
  - integration
domain: Cloud Technology and Services
aliases:
  - "SQS"
  - "SNS"
  - "Kinesis"
  - "Step Functions"
  - "Messaging"
  - "Event-driven"
status: not-started
date: 2026-07-01
---

# Application Integration

## Amazon SQS (Simple Queue Service)

- **Fully managed message queue** service
- **Decouple** application components — producers send messages, consumers poll and process
- Scales from 1 message to 10,000+ messages per second
- Default retention: **4 days** (max: **14 days**)
- Max message size: 256 KB
- Messages can have multiple consumers, but each message is processed **by one consumer**

### SQS Queue Types

| Queue Type | Delivery | Ordering | Throughput | Use Case |
|---|---|---|---|---|
| **Standard Queue** | At-least-once | Best-effort | **Unlimited** | High throughput; order doesn't matter |
| **FIFO Queue** | Exactly-once | Strict FIFO | **3,000 msg/sec** (with batching; 300 API calls × 10 msgs each) | Order matters (financial transactions, deduplication) |

### SQS Visibility Timeout
- When a consumer **receives** a message, it becomes **invisible** to other consumers for the visibility timeout period
- The consumer must **process and delete** the message before the timeout expires
- If not deleted in time, the message becomes **visible again** (another consumer can pick it up)
- This prevents duplicate processing while allowing retry if a consumer crashes
- Default: 30 seconds; configurable from 0 seconds to 12 hours

### SQS Dead Letter Queue (DLQ)
- If a message cannot be processed after a maximum number of retries, it moves to a **dead letter queue**
- Allows you to isolate, inspect, and debug failed messages without blocking the main queue
- Applies to both Standard and FIFO queues

---

## Amazon SNS (Simple Notification Service)

- **Pub/Sub messaging** service
- One message → many receivers (fan-out pattern)
- Creates **topics**; subscribers receive all messages
- Each subscriber processes the message independently

### SNS Subscribers
- Email / Email-JSON
- SMS & Mobile Push Notifications
- HTTP/HTTPS endpoints
- AWS Lambda
- SQS queues
- Kinesis Data Firehose

### SNS Message Filtering
- By default, all subscribers receive every message
- Assign a **filter policy** to a subscription to receive only matching messages
- Filtering is based on message attributes (key-value metadata)

### SNS Dead Letter Queue (DLQ)
- Messages that fail all delivery retries can be sent to a DLQ
- SNS retry policy: 3 immediate → 2 pre-backoff (1s apart) → 10 with exponential backoff → 35 post-backoff (60s apart)
- DLQ enables analysis and manual reprocessing of failed messages

### SQS vs SNS

| Feature | SQS | SNS |
|---|---|---|
| Pattern | Queue (pull) | Pub/Sub (push) |
| Consumers | One consumer per message | All subscribers get message |
| Persistence | Messages persist until consumed | No persistence (fire and forget) |
| Use case | Decouple components; buffer | Fan-out; broadcast notifications |

---

## Amazon Kinesis

- Process **real-time streaming data** at scale
- Use cases: collect, process, and analyze streaming data (logs, IoT, clickstreams)

| Service | Purpose |
|---|---|
| **Kinesis Data Streams** | Real-time data streaming; custom processing |
| **Kinesis Data Firehose** | Load streaming data to S3, Redshift, OpenSearch |
| **Kinesis Data Analytics** | SQL analytics on streaming data |
| **Kinesis Video Streams** | Stream video for ML processing |

---

## Amazon MQ

- Managed **message broker** for Apache ActiveMQ and RabbitMQ
- For applications **migrating from on-premises** that use traditional protocols (MQTT, AMQP, STOMP, OpenWire)
- Does **not scale** as well as SQS/SNS (not serverless)
- Good when you need protocol compatibility with existing systems

> [!tip]
> "A company has an on-premises application using ActiveMQ/RabbitMQ and is migrating to AWS" → Amazon MQ

---

## AWS Step Functions

- **Visual workflows** for orchestrating Lambda functions and other AWS services
- Build serverless workflows as state machines
- Error handling, retries, parallel execution built-in
- Use for: order processing, data pipelines, ML workflows

---

## ML Services Overview

| Service | Input | Output | Use Case |
|---|---|---|---|
| **Rekognition** | Images/Video | Labels, faces, text | Object detection, face search, content moderation |
| **Transcribe** | Audio | Text | Speech-to-text; meeting transcription; PII redaction |
| **Polly** | Text | Audio | Text-to-speech; audiobooks |
| **Translate** | Text | Text | Language translation |
| **Lex** | Voice/Text | Intent | Build chatbots; powers Alexa |
| **Connect** | Customer calls | — | Cloud contact center; integrates with Lex |
| **Comprehend** | Text | Insights | NLP; sentiment, entities, key phrases |
| **SageMaker** | Custom data | ML model | Build, train, and deploy any ML model |
| **Forecast** | Time series data | Predictions | Demand forecasting; 50% more accurate |
| **Kendra** | Documents | Search results | ML-powered enterprise search |
| **Personalize** | User data | Recommendations | Product/content recommendations |
| **Textract** | PDF/Images | Extracted data | OCR + structure extraction (forms, tables) |

---

## Exam Tips

> [!tip]
> - SQS = queue; decouples components; one consumer per message
> - SNS = pub/sub; many subscribers; fan-out notifications
> - SQS FIFO = exact-once delivery, ordered
> - Default SQS retention = 4 days; max = 14 days
> - Amazon MQ = for migrating existing ActiveMQ/RabbitMQ apps
> - Rekognition = images/video analysis
> - Transcribe = audio → text (speech-to-text)
> - Polly = text → audio (text-to-speech)
> - Lex = chatbot engine (powers Alexa)
> - SageMaker = build any custom ML model

## Related Notes
- [[05-Serverless-Containers]]
- [[08-Infrastructure-as-Code]]
