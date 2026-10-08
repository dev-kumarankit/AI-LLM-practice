# LangChain and LangGraph

## Required progression

1. LangChain components, tools and structured outputs.
2. StateGraph, nodes, edges, reducers and conditional routing.
3. Persistent checkpoints and interruption/resume.
4. Short- and long-term memory boundaries.
5. Human approval and tool authorization.
6. Parallel and sequential agents, supervisor patterns and MCP.
7. Agent evaluation, retries, timeouts and budgets.

## Design rule

Use LangGraph only when state, branching, recovery or durable execution are needed. Use plain Python orchestration when the workflow is a single deterministic function or a simple API.

## Required exercises

- Build a workflow with a state schema and explicit transitions.
- Inject a tool failure and verify retry and dead-letter behavior.
- Resume an interrupted workflow from a checkpoint.
- Test unauthorized tool calls and missing approval.
- Compare a direct Python orchestration with LangGraph.
- Record latency, token usage and cost per workflow step.
