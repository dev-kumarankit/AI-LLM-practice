# 36-Week Engineering Roadmap: Python + Node.js + Data Engineering + RAG + LangGraph + Expert AI Systems

## Goal
Build deep engineering skills in **Python and TypeScript**, starting with RAG and LangGraph, progressing through end-to-end **data engineering**, and culminating in reliable, secure, high-scale AI/data platforms. The original first 12 weeks form Phase I; Phases II and III extend it to 36 weeks.

### Starting point
- **Node.js / TypeScript:** Advanced; focus on architecture, AI integrations, performance, and production quality.
- **Python:** Basic; strengthen Python idioms, typing, async programming, FastAPI, and testing.
- **RAG / LangGraph:** Learn fundamentals and progressively build production-style systems.
- **AWS:** Apply existing serverless experience to AI applications and Amazon Bedrock.

**Suggested commitment:** 36 weeks at approximately 2 hours/day (roughly 500 hours if studying 7 days/week). This is a structured path toward advanced competence, not a guarantee of expert-level mastery; production exposure and repeated projects remain essential. Adjust based on progress.

## Phase I — Weeks 1–12: Python, TypeScript, RAG and LangGraph foundations

This is the original roadmap, retained as the prerequisite for the deeper data/AI systems track.

### Weekly roadmap

| Week | Topic | Python track | Node.js / TypeScript track | Deliverable |
|---|---|---|---|---|
| 1 | Python for TypeScript Developers | Typing, functions, collections, classes, dataclasses, exceptions, environments | Compare Python patterns with TypeScript | CLI knowledge-base loader |
| 2 | Python Async + FastAPI | `asyncio`, `await`, HTTPX, Pydantic, FastAPI, pytest | Express vs. FastAPI; concurrency and API architecture | Two REST APIs with matching contracts |
| 3 | LLM Fundamentals | Tokens, prompts, structured outputs, model SDKs, tool calling | Integrate model SDK in TypeScript | Two working LLM chat services |
| 4 | Embeddings and Vector Search | Embeddings, similarity, chunking, pgvector | Index and query vectors in TypeScript | Semantic document search |
| 5 | End-to-End RAG | Ingestion, loaders, chunking, retrievers, source citations | Equivalent TypeScript RAG pipeline | Document Q&A with citations |
| 6 | Advanced RAG | Hybrid search, reranking, metadata filters, retrieval evaluation | Performance profiling, caching, batching | Evaluated and optimized RAG system |
| 7 | LangChain Fundamentals | Models, prompts, retrievers, tools, structured outputs | LangChain.js equivalents | Tool-enabled AI assistant |
| 8 | LangGraph Core | State, nodes, edges, conditional routing, loops | StateGraph workflows in TypeScript | Multi-step workflow |
| 9 | Advanced LangGraph | Checkpoints, persistence, interrupts, human approval | Agent orchestration and failure handling | Persistent research agent |
| 10 | AWS Bedrock + Serverless | Bedrock integration; FastAPI deployment | Lambda, API Gateway, SQS, EventBridge, S3 | Cloud-hosted agent backend |
| 11 | Security + Reliability | Authentication, tenant isolation, evaluation, tracing, tests | Idempotency, retries, observability, CI/CD | Secure production-style agent |
| 12 | Capstone | Polish Python API, tests, processing | Polish TypeScript API, architecture, deployment | Enterprise AI platform |

## Daily study format (approximately 2 hours)

| Time | Activity |
|---|---|
| 30 minutes | Python learning through TypeScript comparisons |
| 30 minutes | AI / RAG / LangGraph concepts |
| 45 minutes | Implement and compare Python and TypeScript code |
| 15 minutes | Tests, debugging, notes, and interview questions |

During Weeks 5–12, shift more time toward hands-on AI implementation and integration.

## Project 1: Enterprise Document RAG (Weeks 1–6)

**Goal:** Ask questions over private documents with grounded, source-cited answers.

Features:
- PDF and text upload, extraction, cleaning, and chunking
- Embedding generation and PostgreSQL + pgvector storage
- Semantic search; hybrid search and reranking as improvements
- Retrieval pipeline with citations and insufficient-context handling
- FastAPI and Node.js/TypeScript versions with comparable endpoints
- Tests and evaluation datasets for retrieval and answer quality

**Definition of done:** Upload a document, ask a question, retrieve relevant passages, and return a cited answer; demonstrate evaluation results on a small test set.

## Project 2: Intelligent LangGraph Agent (Weeks 7–9)

**Goal:** Add tools, decisions, persistence, and human approval to the assistant.

Features:
- Explicit graph state, nodes, edges, and conditional routing
- Document-retrieval tool and one external REST API tool
- Persistent conversations/checkpoints
- Structured outputs and error-handling paths
- Human approval before sensitive side-effecting actions
- Equivalent Python and TypeScript agent workflows

**Definition of done:** Demonstrate multi-step requests where the agent chooses appropriate tools, preserves state, and recovers predictably from errors.

## Project 3: Production AI Platform (Weeks 10–12)

**Goal:** Make the system deployable, observable, and secure.

Features:
- AWS Bedrock integration; S3-based document ingestion
- TypeScript AWS Lambda + API Gateway orchestration, or containerized FastAPI as appropriate
- SQS/EventBridge for asynchronous ingestion events
- AuthN/AuthZ and tenant-specific document isolation
- Secrets management, logging, tracing, retries, and cost monitoring
- Automated tests, Docker, and CI/CD
- RAG evaluation, prompt-injection defenses, and access-control testing

**Definition of done:** Deploy a working demo with documented architecture, repeatable setup, tests, and evidence of retrieval quality and isolation controls.

## Preferred technology stack

| Layer | Technology |
|---|---|
| Languages | Python 3.12+, TypeScript |
| HTTP APIs | FastAPI and Express (or existing Node.js framework) |
| Validation | Pydantic and Zod |
| Orchestration | LangGraph for Python and JavaScript |
| LLM / retrieval helpers | LangChain Python and LangChain.js |
| Database | PostgreSQL + pgvector |
| Cache | Redis, when needed |
| LLM providers | OpenAI initially; AWS Bedrock later |
| Cloud services | AWS Lambda, API Gateway, S3, SQS, EventBridge, Bedrock |
| Tests | pytest; Vitest/Jest; integration tests |
| Delivery | Docker, GitHub Actions |

## Setup checklist

- [ ] Install Python 3.12+ and verify `python --version`
- [ ] Create a Python virtual environment (`python -m venv .venv`)
- [ ] Install Node.js LTS and verify `node --version`
- [ ] Install VS Code, Git, and Docker Desktop
- [ ] Start PostgreSQL with pgvector via Docker when Week 4 begins
- [ ] Create separate `python/` and `typescript/` application directories
- [ ] Add `.env.example`; never commit real API keys
- [ ] Set up code formatting, linting, and testing in both projects
- [ ] Configure model API credentials in Week 3

## Suggested repository structure

```text
enterprise-ai-learning/
├── python/
│   ├── app/
│   ├── tests/
│   ├── pyproject.toml
│   └── .env.example
├── typescript/
│   ├── src/
│   ├── tests/
│   ├── package.json
│   └── .env.example
├── shared/
│   ├── sample-documents/
│   ├── evaluation-cases/
│   └── api-contracts/
├── infra/
│   ├── docker-compose.yml
│   └── aws/
└── README.md
```

## Week 1: Day-by-day starter plan

- **Day 1:** Python variables, types, lists, dictionaries, and functions; compare with TypeScript.
- **Day 2:** Classes, dataclasses, composition, and Python's type hints; compare with TypeScript classes/interfaces.
- **Day 3:** File operations, JSON parsing, exceptions, and context managers.
- **Day 4:** Modules, imports, packages, virtual environments, pip, and project structure.
- **Day 5:** Python generators, comprehensions, and practical data transformations.
- **Day 6:** Build a typed CLI loader that reads sample documents and extracts metadata; implement comparable behavior in TypeScript.
- **Day 7:** Write unit tests, refactor, review differences, and complete a short knowledge check.

## Progress tracker

- [ ] Week 1 — Python for TypeScript Developers
- [ ] Week 2 — Python Async + FastAPI
- [ ] Week 3 — LLM Fundamentals
- [ ] Week 4 — Embeddings and Vector Search
- [ ] Week 5 — End-to-End RAG
- [ ] Week 6 — Advanced RAG
- [ ] Week 7 — LangChain Fundamentals
- [ ] Week 8 — LangGraph Core
- [ ] Week 9 — Advanced LangGraph
- [ ] Week 10 — AWS Bedrock + Serverless
- [ ] Week 11 — Security + Reliability
- [ ] Week 12 — Enterprise AI Capstone

## Learning resources

- Python tutorial: https://docs.python.org/3/tutorial/
- FastAPI tutorial: https://fastapi.tiangolo.com/tutorial/
- LangChain/LangGraph Python: https://docs.langchain.com/oss/python/langgraph/overview
- LangChain/LangGraph JavaScript: https://docs.langchain.com/oss/javascript/langgraph/overview
- PostgreSQL pgvector: https://github.com/pgvector/pgvector
- AWS Bedrock docs: https://docs.aws.amazon.com/bedrock/

---

**Next action:** Begin **Week 1, Day 1**, implementing Python fundamentals next to equivalent TypeScript code. Move to the next week when its deliverable and checks are complete rather than following the calendar rigidly.

See the expanded phases below for the data engineering and expert-specialization path.


---

# Phase II — Weeks 13–24: Data Engineering, Analytics and Real-Time Pipelines

**Outcome:** Design and implement reliable batch and streaming data platforms, and connect them to RAG/agent knowledge systems. Python is the primary implementation language for analytics and ETL; TypeScript remains a first-class language for ingestion APIs, services and orchestration integrations.

| Week | Focus | Python + data engineering | TypeScript + backend engineering | Proof of work |
|---|---|---|---|---|
| 13 | Expert SQL and modeling | CTEs, windows, query plans, normalization, dimensional modeling, SCD Type 1/2 | Parameterized APIs, schema migrations, typed SQL queries | Retail sales star schema + tuned SQL queries |
| 14 | PostgreSQL internals | MVCC, transaction isolation, EXPLAIN ANALYZE, indices, partitioning, vacuum | Connection pools, transaction boundaries, read replicas | Benchmark and optimize a realistic workload |
| 15 | Data ingestion / ELT | Pandas, Polars, Arrow, Parquet, schema validation, incremental loads | REST/webhook ingestion, cursor pagination, rate-limit handling | Idempotent ingest pipeline into raw/staging tables |
| 16 | Orchestration | Apache Airflow DAGs, retries, backfills, dependencies, data contracts | Trigger workflows and expose job health through API | Scheduled incremental ETL with recovery |
| 17 | Transformation + quality | dbt models, tests, documentation, Great Expectations or equivalent | Data contract checks in producers | Tested bronze/silver/gold analytical models |
| 18 | Distributed batch processing | PySpark DataFrames, shuffle, partitions, joins, skew | Integrate a service with batch job status/results | Spark ETL job with runtime/memory profiling |
| 19 | Storage and lakehouses | S3, Parquet partitioning, Iceberg/Delta concepts, schema evolution | Secure ingestion and presigned-upload APIs | Versioned lakehouse-style dataset |
| 20 | Streaming fundamentals | Kafka topics, partitions, consumer groups, offsets, at-least-once | Node Kafka producer/consumer, outbox pattern | Streaming orders/events with deduplication |
| 21 | Stateful stream processing | Event time, watermarks, windowing; Spark Structured Streaming or Flink concepts | Event schema evolution, event contracts | Near-real-time aggregates with late-event tests |
| 22 | Warehouses | Redshift distribution/sort strategies, COPY, query tuning; Snowflake fundamentals | Query-facing analytics APIs and access control | Warehouse load + cost/performance comparison |
| 23 | Cloud data architecture | AWS Glue, Athena, S3, IAM, Step Functions, EventBridge, SQS | Serverless workflow integration and monitoring | Cloud ETL deployment (or local equivalent) |
| 24 | Data platform capstone | Batch + streaming ingestion, quality, lineage, warehouse marts | Dashboard/API and operational endpoints | End-to-end commerce analytics pipeline |

## Data Engineering Capstone — Commerce Data Platform

**Build:** Simulate orders, payments, shipments and customer events. Ingest data through Python batch jobs and TypeScript services; publish events to Kafka; orchestrate transformations with Airflow; validate and model datasets with dbt; query marts with PostgreSQL, Redshift or Snowflake; surface insights through an API.

**Architecture:** Data producers → API/webhooks/Kafka → raw S3/Parquet → Airflow + Spark / Python transforms → warehouse/lakehouse → dbt marts → FastAPI/TypeScript analytics API → monitoring dashboards.

**Expert criteria:** Re-runnable backfills, deduplication, schema-change handling, data-quality checks, documented lineage, measured pipeline latency, query plans and a cost estimate. Distinguish end-to-end exactly-once *effects* achieved with idempotent sinks from a guarantee that all infrastructure delivers exactly once.

# Phase III — Weeks 25–36: Hardcore Systems and Expert AI Engineering

**Outcome:** Advance beyond tutorials into internals, trade-offs, scalability, security, evaluation, performance and incident-response practice. Study Rust selectively only if your target role includes high-performance infrastructure or native systems.

| Week | Expert specialization | What to master | Practical assessment |
|---|---|---|---|
| 25 | Distributed systems foundations | Consistency models, CAP trade-offs, consensus basics, replication, sharding, clocks, failure modes | Write failure-mode and consistency design notes |
| 26 | Performance engineering | Profiling Python and Node, GIL vs event loop, multiprocessing, backpressure, caches, queues | Load-test services and explain bottlenecks with measurements |
| 27 | Advanced Python engineering | Async cancellation, task groups, protocols, generics, dependency injection, package layout, memory profiling | Refactor ingestion and AI APIs with mypy/pytest/benchmarks |
| 28 | Data reliability at scale | CDC, Debezium concepts, outbox/inbox, DLQs, replay, data contracts, evolution | Recover from duplicate events, outages and schema drift |
| 29 | Advanced retrieval systems | Hybrid BM25/vector retrieval, reranking, multi-query, filters, ANN index trade-offs, tenant isolation | Offline relevance evaluation with recall@k / MRR / nDCG |
| 30 | Knowledge graph + GraphRAG | Entity extraction, graph schema, graph retrieval, graph vs vector trade-offs | Compare graph-enhanced retrieval against baseline RAG |
| 31 | Agent architecture | Deterministic workflow vs agent, tool permissions, LangGraph subgraphs, durable execution | Build tool-using agent with constrained actions and checkpoints |
| 32 | AI evaluation + observability | Golden sets, groundedness, tool success, trace inspection, model comparisons, cost/latency budgets | Automated regression suite and evaluation dashboard |
| 33 | AI security | Prompt injection, malicious documents, least privilege, PII, secrets, tenant security, approval gates | Red-team RAG retrieval/tool pathways and document defenses |
| 34 | Advanced model operations | Embedding upgrades, prompt/model versioning, serving patterns, quantization concepts, inference costs | Run an A/B or shadow evaluation with rollback criteria |
| 35 | System design + architecture review | SLA/SLO, capacity estimates, availability, RTO/RPO, cost controls, multi-region trade-offs | Architecture design doc + chaos/failure test |
| 36 | Expert capstone + interview defense | Integrate data + RAG + graph agents, documented operations and trade-offs | Demo, benchmark report, threat model and production runbook |

## Expert Capstone — Real-Time Enterprise Intelligence Platform

Build one system that unifies **data engineering, AI search and AI agents**:

1. **Data plane:** CDC or webhook-based ingestion → Kafka → streaming aggregations → S3/Parquet or Iceberg → warehouse marts.
2. **Knowledge plane:** Document ingestion → extraction/cleaning → versioning → vector + keyword indices → hybrid retrieval → reranking → evaluated citations.
3. **Agent plane:** Python LangGraph workflows with stateful tool usage, human approvals and audit logs; equivalent essential functionality in TypeScript.
4. **Serving plane:** FastAPI plus Node.js BFF services, typed contracts, auth, tenant controls, streaming responses and caching.
5. **Operations plane:** CI/CD, IaC, logs, traces, alerts, SLOs, safe rollouts, load tests and disaster recovery procedures.

**Hardcore pass/fail criteria** (choose realistic target values, then measure rather than inventing results):
- Defend schema and partition/index choices using measured query plans and cost figures.
- Prove a failed or duplicated event can be safely replayed without corrupting final results.
- Report retrieval metrics, answer correctness/groundedness and error categories on a held-out evaluation set.
- Demonstrate tenant isolation, prompt-injection defenses, secret management and auditability.
- Run controlled load tests; document throughput, p50/p95/p99 latency, errors and cost per task.
- Show a recovery runbook, a rollback plan and at least one simulated incident postmortem.
- Explain when a normal pipeline is better than an AI agent and when a graph database is unnecessary.

## Optional Expert Branches (after Week 24, alongside the main path)

- **Data engineer / analytics engineer:** Deeper Spark, Flink, dbt, Iceberg, Redshift, Snowflake, orchestration, governance, cost optimization.
- **AI platform / LLM engineer:** Retrieval science, inference serving, vector indexes, evaluations, RAG security, agents, model serving and cost optimization.
- **Backend / distributed systems architect:** PostgreSQL internals, queues, resilience, caching, capacity planning, event-driven architecture, AWS IaC.
- **Rust (optional, not mandatory):** Ownership/borrowing, Tokio, async services, profiling and Python bindings (PyO3); use for performance-sensitive ingestion/infrastructure components after profiling demonstrates a need.

## Time budget and mastery expectations

At **2 hours/day**, this roadmap is a strong 36-week introduction to advanced practice, but 'hardcore expert' capability normally requires sustained production ownership, debugging real failures and depth in at least one specialization. Spend roughly 60% on implementation, 20% on internals/readings, 10% on tests/benchmarks and 10% on design writing and review. You may require extra weeks for Spark, streaming, warehouse optimization and security.

### Weekly execution pattern

- **Days 1–2:** Read core concepts, draw architecture, implement focused Python examples and compare TypeScript equivalents.
- **Days 3–4:** Implement real pipeline/graph components and automated tests.
- **Day 5:** Add adversarial and failure cases; inspect performance, memory and query plans.
- **Day 6:** Integrate into the main repo; update design docs and metrics.
- **Day 7:** Review, explain trade-offs aloud, and perform a technical interview/architecture defense.

### Expanded repository structure

```text
enterprise-ai-learning/
├── python/                 # FastAPI, data loaders, Spark examples, LangGraph
├── typescript/             # BFF, ingestion, event producers, LangGraph.js
├── data-platform/
│   ├── airflow/
│   ├── dbt/
│   ├── spark/
│   ├── streaming/
│   ├── schemas/
│   └── datasets/
├── rag/
│   ├── ingestion/
│   ├── retrieval/
│   └── evaluation/
├── agents/
├── infra/                  # Docker, IaC, cloud configs
├── load-tests/
├── security-tests/
├── docs/                   # ADRs, SLOs, runbooks, threat models
└── README.md
```

## Progress tracker — additional weeks

- [ ] Week 13 — SQL and modeling
- [ ] Week 14 — PostgreSQL internals
- [ ] Week 15 — Data ingestion and ELT
- [ ] Week 16 — Airflow orchestration
- [ ] Week 17 — dbt and data quality
- [ ] Week 18 — Spark batch processing
- [ ] Week 19 — Lakehouse storage
- [ ] Week 20 — Kafka streaming
- [ ] Week 21 — Stateful streaming
- [ ] Week 22 — Redshift and Snowflake
- [ ] Week 23 — Cloud data architecture
- [ ] Week 24 — Data platform capstone
- [ ] Week 25 — Distributed systems
- [ ] Week 26 — Performance engineering
- [ ] Week 27 — Advanced Python
- [ ] Week 28 — CDC and reliability
- [ ] Week 29 — Advanced retrieval
- [ ] Week 30 — GraphRAG
- [ ] Week 31 — Agent architecture
- [ ] Week 32 — AI evaluation and observability
- [ ] Week 33 — AI security
- [ ] Week 34 — Model operations
- [ ] Week 35 — Architecture review
- [ ] Week 36 — Expert capstone

## Additional references

- Apache Spark: https://spark.apache.org/docs/latest/
- Apache Airflow: https://airflow.apache.org/docs/
- Apache Kafka: https://kafka.apache.org/documentation/
- dbt: https://docs.getdbt.com/
- Apache Iceberg: https://iceberg.apache.org/docs/latest/
- AWS Redshift: https://docs.aws.amazon.com/redshift/
- Snowflake: https://docs.snowflake.com/
- PostgreSQL: https://www.postgresql.org/docs/
- Python asyncio: https://docs.python.org/3/library/asyncio.html
