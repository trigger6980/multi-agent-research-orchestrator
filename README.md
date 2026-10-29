# Multi-Agent Research Orchestrator

Hierarchical multi-agent system for reliable research synthesis.

**Pipeline:** plan → parallel research (independence gate) → synthesize → critique → revise → verify

## Features

- Specialist agents: Planner, Researcher, Synthesizer, Skeptic, Verifier
- Independence gate for safe parallel dispatch
- Full audit trail of every agent action
- Dual runtime: pure Python + optional LangGraph
- Pluggable LLM backends: stub / openai / anthropic / xai
- Evaluation harness (20 questions) multi-agent vs single-agent
- Metrics: citation accuracy, groundedness, coherence, coverage, **verified**
- Stub baseline result: multi verified = 1.0 vs single = 0.0 (Δ +1.0)
- Thesis outline + one-page abstract
- Live baseline runbook
- Makefile + GitHub Actions CI

## Quick start

```bash
git clone https://github.com/trigger6980/multi-agent-research-orchestrator
cd multi-agent-research-orchestrator
pip install -e ".[dev]"
make test
PYTHONPATH=src python scripts/demo.py "What are failure modes of multi-agent LLMs?"
```

## Docs

- [Abstract](docs/ABSTRACT.md)
- [Thesis outline](docs/THESIS_OUTLINE.md)
- [Live baseline runbook](docs/LIVE_BASELINE.md)
- [Architecture](docs/ARCHITECTURE.md)

## Related

- Prior private repo: [agentic-research-orchestrator](https://github.com/trigger6980/agentic-research-orchestrator)
- Controller: [github-controller](https://github.com/trigger6980/github-controller)
- Index: [repo-index](https://github.com/trigger6980/repo-index)

MIT License
