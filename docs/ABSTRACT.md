# Abstract

**Title.** Hierarchical Multi-Agent Orchestration for Reliable Research Synthesis: Independence Gates, Adversarial Critique, and Verification-Before-Completion

Large language models are increasingly used as research assistants, yet single-agent pipelines remain prone to unsupported claims, weak citation discipline, and the absence of adversarial review. This work presents a hierarchical multi-agent system that treats research synthesis as a coordinated workflow rather than a single generation step. A parent orchestrator decomposes a query into a task graph, dispatches specialist researchers under an independence gate that admits parallel execution only when ownership and dependency constraints allow, then merges findings through a synthesizer. An adversarial skeptic critiques the draft; the synthesizer revises; a verifier blocks completion when citations or claims fail structural checks. The system exposes a dual runtime (pure Python and optional LangGraph), pluggable LLM backends (stub, OpenAI, Anthropic, xAI), git worktree isolation helpers for file-writing agents, and a full audit trail of agent actions.

Evaluation uses twenty curated research questions. We compare the multi-agent pipeline against a single-agent one-shot baseline. On a deterministic offline stub backend (n = 20), content metrics are matched by construction, while verification rate separates the conditions cleanly: multi-agent achieves verified = 1.0 versus single-agent verified = 0.0 (Δ = +1.0). This demonstrates that verification-before-completion is enforced by architecture, independent of model quality.

**Contributions.** (1) Reproducible hierarchical orchestration with independence gating, critique, and verification. (2) Evaluation harness and baseline comparison with committed results. (3) Dual runtime and agent definitions for transfer into coding-agent environments.

**Keywords.** multi-agent systems; LLM agents; verification; research synthesis; evaluation harness; independence gate
