# Advanced RAG Engineering

## Required progression

1. Document ingestion and source provenance.
2. PDF, DOCX, HTML, Markdown and JSON parsing.
3. OCR and multimodal boundaries.
4. Chunking, embeddings and similarity metrics.
5. pgvector, OpenSearch and managed alternatives.
6. Metadata, tenant filtering, BM25 and hybrid retrieval.
7. Reranking, query transformation and context compression.
8. Retrieval evaluation, citations and groundedness.

## Evaluation before complexity

Build a fixed evaluation set before adding advanced retrieval patterns. Measure recall@k, MRR, nDCG, answer groundedness, citation correctness, latency and cost.

## Required exercises

- Ingest a small document set and record source/version metadata.
- Compare semantic, keyword and hybrid retrieval.
- Test missing context and unauthorized documents.
- Add a retrieval cache and incremental indexing policy.
- Validate that citations point to the exact retrieved source.
- Run a red-team prompt-injection test against retrieval context.
