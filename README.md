# Data Engineering Notes

## Overview

This roadmap is based off resources I have researched, data engineers I have spoken with through LinkedIn, and the data engineer roadmap.sh.

AI was used to create the outline based off the data I presented it with, but the notes themselves are written and researched by me. AI is used to help organize structure and improve clarity, not to generate the core content.

To go along with these notes, I maintain a separate repository containing projects and small demos for concepts I’ve learned and implemented.

This repository is focused on understanding data engineering from a systems perspective — not just learning tools.

---

## Purpose

This repository exists to:

* Build structured knowledge in data engineering
* Strengthen SQL and data modeling fundamentals
* Understand how real data systems are designed and scaled
* Prepare for junior-to-mid level data engineering roles
* Develop clear, interview-ready explanations of core systems

Each section follows the data engineering lifecycle and builds upward from foundations to production-level systems.

---

## Structure

The notes follow this progression.

### 0. Pre-Requisites

Programming and systems foundations:

* Python (primary language)
* Java / Scala / Go (awareness)
* Data Structures and Algorithms
* Git and GitHub
* Linux basics
* Networking fundamentals
* Distributed systems basics

---

### 1. What is Data Engineering

* What is Data Engineering?
* Data Engineering vs Data Science
* Skills and Responsibilities
* The Data Engineering Lifecycle
* Choosing the right technologies

---

### 2. The Data Engineering Lifecycle

The lifecycle is broken into four stages:

1. Data Generation
2. Data Storage
3. Data Ingestion
4. Data Serving

Each stage is studied conceptually and then connected to implementation.

---

### 3. Data Generation

* Sources of data (databases, APIs, logs, mobile apps, IoT)
* Data collection considerations
* Volume, schema design, and data quality at source

---

### 4. Data Storage

Core database fundamentals:

* Data normalization
* Data modeling techniques
* CAP theorem
* OLTP vs OLAP
* Slowly Changing Dimensions (SCD)
* Horizontal vs vertical scaling
* Star vs snowflake schema
* Indexing
* Transactions

Relational databases:

* PostgreSQL
* MySQL
* MariaDB
* Oracle
* MS SQL
* Aurora

NoSQL databases:

* Document (MongoDB, CouchDB, CosmosDB, Elasticsearch)
* Column (Cassandra, BigTable, HBase)
* Graph (Neo4j, Neptune)
* Key-value (Redis, Memcached, DynamoDB)

---

### 5. Data Warehousing and Architectures

* What is a data warehouse
* Data warehouse architectures
* Data marts
* Data lakes
* Delta Lake
* Data mesh
* Data fabric
* Metadata-first architecture
* Serverless options

Platforms:

* BigQuery
* Snowflake
* Redshift
* Databricks

---

### 6. Cloud Computing

Cloud fundamentals:

* Compute vs storage
* Managed services
* Serverless patterns
* Cloud-native architecture

Providers:

* AWS (EC2, S3, RDS, Glue)
* Azure (VMs, Blob Storage, Azure SQL, Data Factory)
* Google Cloud (Compute Engine, Cloud Storage, Cloud SQL, Dataflow)

---

### 7. Data Ingestion

* Batch ingestion
* Streaming ingestion
* Hybrid pipelines
* Real-time pipelines
* ETL vs ELT

Pipeline tools:

* Airflow
* dbt
* Luigi
* Prefect

---

### 8. Cluster and Distributed Computing

* Cluster computing fundamentals
* Distributed file systems
* Job scheduling
* Cluster management

Tools:

* Kubernetes
* Hadoop YARN
* HDFS
* Apache Spark

---

### 9. Containers and CI/CD

* Docker
* Kubernetes
* GKE
* EKS
* CI/CD pipelines

  * GitHub Actions
  * GitLab CI
  * CircleCI
  * ArgoCD

---

### 10. Monitoring and Testing

Monitoring:

* Prometheus
* Datadog
* Sentry
* New Relic

Testing:

* Unit testing
* Integration testing
* End-to-end testing
* Load testing
* Smoke testing

---

### 11. Messaging Systems

* Asynchronous vs synchronous communication
* Messages vs streams
* Best practices

Tools:

* Kafka
* RabbitMQ
* AWS SQS
* AWS SNS

---

### 12. Infrastructure as Code

* Declarative vs imperative approaches
* Idempotency
* Environment management
* Reusability

Tools:

* Terraform
* OpenTofu
* AWS CDK
* Google Deployment Manager

---

### 13. Data Serving and Analytics

* Business intelligence
* Reverse ETL
* Data analytics layer

Tools:

* Power BI
* Tableau
* Looker
* Streamlit

---

### 14. Security and Governance

* Authentication vs authorization
* Encryption
* Tokenization
* Data masking
* Data governance
* Data lineage
* Metadata management
* Data interoperability

Regulation:

* GDPR
* ECPA
* EU AI Act

---

## How This Repository Is Used

Each topic includes:

* Definition
* Why it matters
* How it works
* Tradeoffs
* Interview explanation
* Where it fits in the lifecycle
* Link to related implementation project

Concepts are reinforced through small demos and larger pipeline integrations in a separate repository.

---

## Related Repositories

* Data engineering projects (concept demos and implementations)
* Letterboxd ELT Pipeline (production-style system)
* SQL notes (advanced SQL foundation)

---

