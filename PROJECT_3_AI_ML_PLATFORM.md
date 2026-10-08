# Project 3 — Cloud-Native AI/ML Intelligence Platform

## Purpose

Combine governed data, model training, reproducible inference, retrieval-augmented agents and cloud operations into one integrated intelligence platform.

## Architecture

```text
Project 2 data and feature pipeline
             │
             ▼
Model training and experiment tracking
             │
             ▼
Model registry and release candidate
             │
             ▼
Batch and real-time inference services
             │
             ▼
LangGraph agent and approved analytics tools
             │
             ▼
Next.js dashboard and analytics API
```

## Implementation phases

1. **Data foundations:** reuse curated data, feature contracts and quality checks.
2. **Training:** PyTorch or scikit-learn pipeline with reproducible dependencies and data versions.
3. **Tracking:** MLflow experiments, artifacts, metrics and model registry.
4. **Inference:** batch and online prediction APIs with latency and cost budgets.
5. **Agents:** RAG-assisted analytical explanations and approved API tool calls.
6. **Cloud:** AWS Bedrock, ECS/EKS or serverless, Terraform/CDK and GitHub Actions.
7. **Operations:** distributed tracing, model drift, rollback and incident runbooks.

## Required controls

- Model and prompt versions in every request response.
- Evaluation datasets and regression gates.
- Drift and data-quality monitoring.
- Human approval for sensitive actions.
- Secrets and model access isolated from application code.
- Cost, latency and throughput budgets.
- Rollback and retraining procedures.

## Acceptance criteria

- A training run can be reproduced from configuration and inputs.
- A registered model can be promoted, tested and rolled back.
- The agent can explain analytical results with source provenance.
- Batch and real-time inference have measured latency and cost.
- The system passes security, quality and deployment gates.
