# Master Roadmap — 48–60 Week Advanced AI, Data, Cloud and Distributed Systems Program

> **Status:** v1.0 — curriculum architecture and project mapping  
> **Target:** 48 weeks, expandable to 60 weeks when a topic requires deeper implementation  
> **Weekly commitment:** 2 hours/day, 6 days/week, approximately 576 hours  
> **Primary languages:** Python and TypeScript/Node.js  
> **Primary AI runtime:** Python for model, RAG, data and orchestration work; TypeScript for APIs, BFFs, agents and UI boundaries

## 1. Critical audit of the previous roadmap

### Missing or underdeveloped areas

- **Python internals:** GIL, memory management, garbage collection, profiling, process/thread boundaries and cancellation are currently treated as awareness topics rather than exercises.
- **Security engineering:** guardrails are not a standalone design module. They must be part of every AI service and capstone workflow.
- **Evaluation:** retrieval, model, agent, security and pipeline evaluations need fixed datasets, quality gates and measured baselines.
- **System design:** the roadmap needs explicit architecture reviews, failure modes, consistency, backpressure, replication and operating objectives.
- **Production engineering:** every major feature must include tests, observability, failure recovery, performance and deployment evidence.
- **Architecture mapping:** project tasks must map to week-level learning rather than simply replacing the roadmap with a product checklist.

### Redundancies

- The roadmap repeats model and RAG concepts across weeks 9–34. Each repetition should move the learner from a small API example to a production control point.
- LangChain and LangGraph should not be taught as separate broad subjects. Learn the minimum LangChain components needed to integrate LangGraph, tools, structured outputs and MCP.
- Multiple cloud providers should be introduced through architecture comparisons, not equal implementation depth. AWS is the primary platform; Azure and GCP are optional comparison tracks.

### Learning-order corrections

1. Programming and testing fundamentals.
2. SQL, HTTP, networking, Linux, Docker and basic service reliability.
3. Python AI and retrieval foundations.
4. RAG evaluation and safe stateful agents.
5. Data engineering batch and streaming foundations.
6. Model engineering and LLMOps.
7. Distributed systems, AWS, security and observability.
8. Three integrated capstones and final expert review.

### Removed or reduced breadth

- Rust is optional and should not block Python or TypeScript progress.
- GraphRAG is elective after baseline RAG and evaluation are working.
- LlamaIndex, Dagster, Flink, Snowflake and Databricks are optional comparisons rather than required deep tracks.
- A language implementation should be introduced only when it teaches an architecture or control boundary that Python alone cannot demonstrate.

## 2. Expected expertise outcomes

By the end of the program, the learner should be able to:

- Build typed Python services with FastAPI, async APIs, modular architecture, testing and operational controls.
- Build and evaluate RAG systems using chunking, embeddings, hybrid retrieval, metadata filtering, citations and tenant-aware controls.
- Design safe LangGraph workflows with checkpoints, tool authorization, human approval, timeouts, retries and interruption recovery.
- Implement batch, streaming and lakehouse pipelines using SQL, Spark, Kafka, Airflow, dbt and governed storage.
- Build model and LLM lifecycle pipelines with experiment tracking, evaluation gates, monitoring and rollback.
- Design enterprise AWS systems with IAM, networking, queues, observability, IaC, load testing and disaster recovery.
- Independently debug failures across services, databases, model providers, retrieval, queues and infrastructure.
- Provide architecture reviews, ADRs, threat models, runbooks, performance evidence and cost estimates.

## 3. Phase structure

| Phase | Weeks | Primary outcome |
|---|---:|---|
| I — Python and service foundations | 1–8 | Typed, tested and profiled Python services |
| II — RAG and agentic AI | 9–16 | Evaluated, secure and stateful AI workflows |
| III — Data engineering | 17–26 | Reliable batch, streaming and lakehouse platform |
| IV — Model engineering and LLMOps | 27–34 | Reproducible model and prompting lifecycle |
| V — Distributed systems and cloud | 35–42 | Observable, resilient AWS platform |
| VI — Integration and expert capstone | 43–48 | Enterprise intelligence platform with evidence |

## 4. curriculum dependency map

```text
Python + SQL + HTTP
        ↓
FastAPI / typing / tests / observability
        ↓
RAG ingestion + embeddings + retrieval evaluation
        ↓
LangGraph + tools + security + checkpoints
        ↓
Kafka + CDC + Spark + Airflow + dbt
        ↓
Lakehouse + warehouse + governed data
        ↓
PyTorch / HF / model evaluation / MLflow
        ↓
AWS architecture / IaC / Kubernetes / tracing
        ↓
Integrated AI + data + cloud platform
```

## 5. Weekly study model

| Day | Activity |
|---|---|
| Monday | Learn concept and complete a focused Python exercise |
| Tuesday | Build a service component with TypeScript comparison where useful |
| Wednesday | Implement data, AI or model behavior and record the data path |
| Thursday | Test, debug, profile and measure the implementation |
| Friday | Architecture, security and distributed-systems review |
| Saturday | Complete weekly deliverable, documentation and repository commit |
| Sunday | Rest, retrospective or catch-up |

Every week must produce:

1. A short concept note.
2. A code change with tests.
3. A realistic failure or edge-case test.
4. A performance or security measurement where applicable.
5. An architecture decision or tradeoff note.
6. A commit and a weekly evidence record.

## 6. 48-week curriculum

### Weeks 1–8 — Python, backend foundations and service reliability

| Week | Objectives | Python | TypeScript / Node | Exercises and deliverable |
|---:|---|---|---|---|
| 1 | Python syntax, collections, functions, exceptions, packaging | Deep equality, configuration parsing, typed domain models | Compare Python and TypeScript scalar/type behavior | CLI ingestion service with tests |
| 2 | OOP, dataclasses, Pydantic, context managers, dependency injection | Package and validate domain events | Define matching OpenAPI contract | Tested Python package and API schema |
| 3 | Asyncio, generators, threads, processes, cancellation, GIL | Concurrent I/O and CPU benchmark | Compare Node event loop and worker threads | Concurrency benchmark with failure cases |
| 4 | FastAPI, dependencies, HTTPX, auth, structured errors | Typed API with Pydantic and async dependencies | BFF and TypeScript API contract | FastAPI service with integration tests |
| 5 | SQL, indexes, transactions, isolation, EXPLAIN | SQLAlchemy and PostgreSQL query design | ORM or driver comparison; N+1 analysis | Query plan and index report |
| 6 | Linux, networking, TLS, HTTP, containers and debugging | Profile service CPU/memory and logs | Load-test Node and Python endpoints | Troubleshooting runbook |
| 7 | DSA, complexity, hashing, trees, graphs, pytest | Implement sorting, graph and data-structure algorithms | Compare operational complexity in TS | Algorithm suite and property tests |
| 8 | Profiling, memory, packaging, deployment | Optimize a typed API using profiling | Compare deployment and lifecycle controls | Measured performance and release artifact |

### Weeks 9–16 — RAG, retrieval and agentic AI

| Week | Objectives | Python | TypeScript / Node | Deliverable |
|---:|---|---|---|---|
| 9 | Tokens, context, model abstraction, structured output, tool interfaces | Model gateway and tool schemas | TypeScript gateway and retry policy | Model-agnostic chat API |
| 10 | Embeddings, chunking, pgvector and similarity | Ingest and retrieve documents with metadata | Shared retrieval API and contract | Baseline semantic search |
| 11 | Document ingestion, PDF/DOCX/HTML/Markdown/JSON, OCR and provenance | Incremental workers and source metadata | Upload event and async processing contract | Citation-aware ingestion pipeline |
| 12 | Hybrid retrieval, BM25, RRF, reranking, query rewriting | Compare retrieval strategies | Latency/cost instrumentation | Retrieval experiment report |
| 13 | Retrieval evaluation, gold datasets, recall@k, groundedness and citation correctness | Build fixed evaluation suite | Evaluation dashboard API | Measurable retrieval baseline |
| 14 | LangChain components, tools, structured outputs, MCP | Use only required LangChain components | Compare LangChain.js and Python behavior | Tool-enabled assistant |
| 15 | LangGraph state, nodes, edges, routing, reducers and loops | Stateful multi-step workflow | Equivalent TypeScript workflow | Integration-tested graph |
| 16 | Checkpoints, interrupts, approvals, persistence, security | Agent with explicit permissions and recovery | Tool-policy and audit integration | Secure RAG + agent release |

### Weeks 17–26 — Data engineering and lakehouse

| Week | Objectives | Python | TypeScript / Node | Deliverable |
|---:|---|---|---|---|
| 17 | ETL/ELT, data modeling and contracts | Bronze/silver/gold transformations | Event schema and API contracts | Analytical model and lineage |
| 18 | Advanced SQL, window functions, PostgreSQL and Redshift | Query tuning and explain plans | Migration validation | SQL performance suite |
| 19 | Spark architecture, partitions, transforms and skew | Batch pipeline | Worker/resource contract | Reproducible Spark job |
| 20 | Spark DAG, Catalyst, shuffle, join and partition tuning | Compare before/after plans | Cost and resource report | Optimized Spark benchmark |
| 21 | Airflow, retries, backfills, idempotency and recovery | Scheduled data pipeline | Event handoff and status API | Reliable pipeline runbook |
| 22 | dbt, tests, contracts, lineage and documentation | Quality and freshness tests | Data quality API | Versioned warehouse models |
| 23 | Kafka offsets, partitions, ordering, consumer groups and delivery semantics | Kafka consumer and replay | Producer with outbox | Streaming workflow |
| 24 | CDC, Debezium, outbox, schema evolution and reconciliation | CDC ingestion and deduplication | Transactional event producer | Recovery-tested CDC pipeline |
| 25 | Parquet, Delta/Iceberg, lakehouse patterns | Incremental lakehouse jobs | Storage and cost review | Lakehouse implementation |
| 26 | Redshift, Snowflake, governance and lineage | Warehouse comparison and RBAC | Data ownership and access review | Data platform capstone |

### Weeks 27–34 — Models, LLMOps and ML lifecycle

| Week | Objectives | Python | TypeScript / Node | Deliverable |
|---:|---|---|---|---|
| 27 | Linear algebra, probability, optimization, PyTorch | Tensor/autograd and attention prototype | Model-serving API contract | Reproducible learning notebook |
| 28 | Hugging Face, tokenization, embeddings and evaluation | Pretrained inference experiment | Hosted/open model comparison | Model evaluation report |
| 29 | Rerankers, domain adaptation and embeddings | Entity/semantic evaluation | API/client benchmark | Retrieval model benchmark |
| 30 | Fine-tuning, PEFT/LoRA and dataset quality | Controlled adapter experiment | Risk and cost decision | Fine-tuning decision memo |
| 31 | Batching, quantization, vLLM and inference | Serving benchmark | Timeout, concurrency and gateway policy | Inference performance report |
| 32 | MLflow, datasets, artifacts, registries and versioning | Reproducible experiments | Release and model contract | Versioned model pipeline |
| 33 | Prompt versioning, evaluation gates, tracing and drift | Offline regression suite | Provider/tool failure handling | LLM CI gate |
| 34 | Hallucination, prompt injection, safety, leakage and red-teaming | Security and output evaluation | Audit and guardrail integration | Hardened model service |

### Weeks 35–42 — Distributed systems, AWS, security and operations

| Week | Objectives | Python | TypeScript / Node | Deliverable |
|---:|---|---|---|---|
| 35 | CAP, consistency, idempotency, transactions and partitions | Idempotent worker prototype | Event schema and consistency design | Distributed design document |
| 36 | Queues, backpressure, retry, DLQ, ordering and recovery | Resilient worker | SQS/EventBridge integration | Fault-injection report |
| 37 | Logs, metrics, tracing, SLO/SLI and OpenTelemetry | Instrument Python service | Correlate TypeScript traces | Operational dashboard |
| 38 | Kubernetes, containers, probes, scaling and deployments | Containerize service | Compare serverless and K8s | Deployable manifests |
| 39 | Terraform/CDK, IAM, networking and secrets | Infrastructure code | TypeScript service stack | IaC review and validated plan |
| 40 | AWS Bedrock, S3, Glue, Redshift, Lambda and SQS | Cloud data and AI integration | Event-driven API implementation | Cloud integration demo |
| 41 | Load testing, capacity, p50/p95/p99, cost | Performance benchmark | Node profile and API analysis | Performance budget report |
| 42 | Tenancy, encryption, secrets, chaos and recovery | Security and restore exercises | IAM and CI controls | Production-readiness scorecard |

### Weeks 43–48 — Integrated capstone and expert review

| Week | Objectives | Deliverable |
|---:|---|---|
| 43 | Architecture, nonfunctional requirements and ADRs | Decision records and target architecture |
| 44 | Ingestion across documents, CDC and streaming | End-to-end ingestion evidence |
| 45 | Search, retrieval, agents and permissions | Evaluated, secure Q&A workflow |
| 46 | Deployment, access control, monitoring and CI/CD | Repeatable deployment and runbook |
| 47 | Load, chaos, backfill, cost and recovery | Measured resilience and cost report |
| 48 | Final review, portfolio and operator readiness | Demo, scorecard, architecture defense and documentation |

## 7. Three mandatory project specifications

### Project 1 — Secure Enterprise RAG and Agentic AI Platform

**Architecture:** Next.js dashboard → TypeScript BFF → Python FastAPI/LangGraph → model provider → vector retrieval/tool services.

**Required:**

- Document upload to S3 and asynchronous processing.
- PDF, DOCX, HTML, Markdown and JSON ingestion.
- PostgreSQL/pgvector and optional OpenSearch.
- Hybrid retrieval, reranking, citations and tenant ACLs.
- Persistent LangGraph checkpoints and human approval.
- Prompt injection, PII, tool abuse and data exfiltration tests.
- Bedrock Guardrails, audit logs and observability.
- CI/CD, Docker and cloud deployment.

**Acceptance criteria:** retrieval metrics, grounding, latency, cost, security passes, recovery and API documentation are recorded and reproducible.

### Project 2 — Real-Time Enterprise Data Engineering Platform

**Architecture:** Node.js producers and PostgreSQL CDC → Kafka → Spark → S3 lakehouse → Redshift → analytics API → Next.js dashboard.

**Required:**

- Outbox and CDC, deduplication, replay and late-event handling.
- Spark batch and streaming jobs.
- Airflow orchestration, dbt transformations and data quality tests.
- Schema evolution, lineage, backfills and access control.
- Failure injection and recovery tests.
- Throughput, lag, correctness, recovery and cost measurements.

**Acceptance criteria:** source-to-target reconciliation, quality gates, plan evidence and replay behavior are demonstrated.

### Project 3 — Cloud-Native AI/ML Intelligence Platform

**Architecture:** Data platform → feature pipeline → model training/registry → inference → LangGraph agents → full-stack dashboard.

**Required:**

- Reuse data from Project 2.
- MLflow experiments, model registry and reproducible training.
- Batch and real-time inference.
- RAG context for analytical results and approved tool access.
- Bedrock, Terraform/CDK and GitHub Actions.
- Distributed tracing, metrics, security and capacity testing.

**Acceptance criteria:** reproducibility, model quality, inference latency, security, operating cost and rollback behavior are demonstrated.

## 8. Assessment and expert-readiness scorecard

Rate each capability from 0 to 4:

- 0: no exposure.
- 1: can explain.
- 2: can implement with guidance.
- 3: can independently design and debug.
- 4: can operate, optimize, compare and teach using measured evidence.

| Capability | Evidence |
|---|---|
| Python and service reliability | Typed API, tests, profiling and failure recovery |
| TypeScript architecture | BFF/API contracts and strict typing |
| SQL and data modeling | Query plans, indexes, migrations and quality tests |
| Spark and streaming | Plans, throughput, lag and replay evidence |
| RAG and agents | Retrieval metrics, citations, security and checkpoint tests |
| Model and LLM lifecycle | Experiments, eval gates, monitoring and rollback |
| Cloud and distributed design | ADRs, load tests and operating runbooks |
| Security and governance | Threat model, authorization tests and audit logs |
| Observability and cost | Dashboards, SLOs and cost estimates |

## 9. Required engineering standards

- Architecture diagrams, repository structure, API specifications, migrations and schemas.
- Unit, integration and end-to-end tests.
- Security tests, CI/CD, environment configuration and Docker.
- Logging, tracing, metrics, load tests and recovery.
- Measured performance, reliability and cost targets before implementation.
- ADRs explaining reasons for technology selection.
- No credential exposure or fabricated benchmark results.

## 10. Official resources

- Python documentation: https://docs.python.org/3/
- FastAPI: https://fastapi.tiangolo.com/
- LangGraph: https://docs.langchain.com/oss/python/langgraph/overview
- LangChain: https://docs.langchain.com/oss/python/langchain/overview
- PostgreSQL: https://www.postgresql.org/docs/
- pgvector: https://github.com/pgvector/pgvector
- Spark: https://spark.apache.org/docs/latest/
- Kafka: https://kafka.apache.org/documentation/
- Airflow: https://airflow.apache.org/docs/
- dbt: https://docs.getdbt.com/
- Debezium: https://debezium.io/documentation/
- PyTorch: https://pytorch.org/docs/stable/
- Hugging Face: https://huggingface.co/docs
- MLflow: https://mlflow.org/docs/latest/
- OpenTelemetry: https://opentelemetry.io/docs/
- AWS Bedrock: https://docs.aws.amazon.com/bedrock/

## 11. Completion rule

A week is complete only after the learner has a commit, automated tests, a short summary, a design or measurement artifact, and a reviewed failure or tradeoff. Completion of the curriculum does not equal expert status; operational ownership and independent production work remain the final qualification.
