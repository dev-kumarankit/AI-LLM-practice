# Project 2 — Real-Time Enterprise Data Engineering Platform

## Purpose

Build a reliable batch and streaming platform that converts operational events into governed analytical data with replay, recovery, quality checks and observable cost.

## Architecture

```text
Node.js producer / PostgreSQL CDC
             │
             ▼
Kafka topic and consumer groups
             │
             ▼
Spark batch and streaming jobs
             │
             ▼
S3 lakehouse / Delta or Iceberg
             │
             ▼
Redshift or Snowflake warehouse
             │
             ▼
Analytics API and Next.js dashboard
```

## Implementation phases

1. **Contracts:** event schema, outbox, database mappings and version compatibility.
2. **Streaming:** Kafka producer/consumer, ordering, offsets, deduplication and replay.
3. **CDC:** Debezium, schema evolution, source-to-target reconciliation and late events.
4. **Batch:** PySpark jobs, partitions, transformations, backfills and quality checks.
5. **Lakehouse:** Parquet, retention, incremental updates and lineage.
6. **Warehouse:** Redshift optimization, dbt models and access control.
7. **Operations:** Airflow, monitoring, failover, recovery and cost analysis.

## Test and validation requirements

- Source-to-target record and aggregate reconciliation.
- Duplicate and out-of-order event tests.
- Repeated processing without corrupting aggregate results.
- Schema compatibility and migration tests.
- Spark plan and skew evidence.
- Kafka lag and processing-lag alerts.
- Backfill and replay runbook.
- Data-quality test pass/fail metrics and lineages.

## Acceptance criteria

- Every event is processed at least once, with at-least-once semantics and explicit idempotency.
- Quality tests prevent invalid records from entering the analytical layer.
- Replay does not produce duplicate business aggregates.
- Pipeline throughput, lag, recovery and cost are measured.
- Operational ownership, lineage and access policy are documented.
