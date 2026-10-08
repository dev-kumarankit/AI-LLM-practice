# Advanced Python Engineering

## Core progression

1. Syntax, functions, collections and exceptions.
2. Dataclasses, Pydantic, protocols, typed dictionaries and generics.
3. Decorators, iterators, generators and context managers.
4. Asyncio, threads, processes, cancellation and the GIL.
5. Memory, garbage collection and profiling.
6. FastAPI, SQLAlchemy, Alembic and dependency injection.
7. Pytest, fixtures, mocking, property tests and coverage.
8. Ruff, mypy/pyright, packaging and reproducible environments.
9. Clean architecture, design patterns and dependency boundaries.

## Python versus TypeScript decisions

- Use Python for data processing, model execution and retrieval.
- Use TypeScript for API contracts, orchestration and user-facing integrations.
- Compare type behavior, exception handling, async runtimes and serialization.
- Do not duplicate the same algorithm in both languages without a different architectural lesson.

## Required exercises

- Build a typed FastAPI API with Pydantic validation.
- Implement a context-managed connection and a retry policy.
- Compare thread and process behavior for a CPU-bound task.
- Profile memory and CPU with a real workload.
- Add tests for invalid input, timeout, cancellation and dependency failure.
- Add a package, lint, type-check and test command to the repository.
