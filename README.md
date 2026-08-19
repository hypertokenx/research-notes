# Research Notes

A collection of research notes on AI systems, LLM reliability, retrieval, hallucinations, evaluation, and forecasting under uncertainty.

The repository is designed to demonstrate **research synthesis** rather than simple summarization.

## Research Method

Each note follows a common structure:

1. **Start with a research question.**
2. **Establish the earlier understanding** using foundational research.
3. **Examine newer evidence**, with emphasis on 2025–2026 work where available.
4. **Compare the evidence over time.**
5. **Identify what changed**: confirmed, weakened, overturned, or complicated.
6. **Separate observation from interpretation.**
7. **State the current assessment and remaining uncertainty.**
8. **Consider practical implications.**

The goal is not to claim that the latest paper automatically supersedes earlier work. Instead, newer evidence is used to test whether earlier conclusions still hold.

## Contents

- `llm-limitations.md` — How rapid capability gains have changed the traditional picture of LLM limitations
- `ai-evaluation.md` — Why increasingly capable AI systems require evaluation beyond headline benchmark scores
- `rag-overview.md` — How retrieval-augmented generation evolved and why retrieval does not guarantee grounded answers
- `llm-hallucinations.md` — How factual reliability has improved while unsupported generation remains a measurable problem
- `forecasting-and-model-uncertainty.md` — What probabilistic forecasting teaches about calibration, uncertainty, metrics, and decisions

## Cross-Cutting Question

The notes examine different versions of one broader question:

> **How should we determine whether a model's output deserves our confidence?**

Across the repository, this becomes:

**Capability → Evidence → Uncertainty → Reliability → Decision**

## Source Standards

Sources are grouped conceptually into:

- **Foundational research** — original or widely cited work that established important concepts
- **Recent independent research** — newer academic work testing or extending earlier findings
- **Institutional research** — organizations such as NIST and ECMWF
- **Primary vendor evidence** — model cards and system cards describing vendor-run evaluations

Vendor-reported results are treated as evidence of what the vendor measured, not as independent confirmation of every broader capability claim.

## Limitations

These notes are analytical research summaries, not systematic literature reviews. Source selection is necessarily limited, and conclusions may change as evidence develops.

**Research status: August 2026.**
