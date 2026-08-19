# Research Notes

A collection of research notes exploring AI systems, LLM reliability, retrieval, hallucinations, and forecasting under uncertainty.

The repository focuses on **research synthesis rather than simple summarization**: comparing evidence from multiple sources, distinguishing capability from reliability, identifying competing explanations, and drawing conclusions that remain appropriately qualified.

## Research Approach

Each note follows a general framework:

1. **Define the question** — Identify the specific problem being investigated.
2. **Establish the current state of evidence** — Prioritize recent research, technical reports, primary sources, and authoritative institutions.
3. **Separate capability from reliability** — A system performing well on a benchmark does not automatically establish robustness in other settings.
4. **Compare evidence** — Look for agreement, disagreement, trade-offs, and changes over time.
5. **Synthesize** — Draw a broader conclusion from the evidence rather than simply summarizing individual sources.
6. **Identify uncertainty** — Distinguish established findings from plausible interpretations and unresolved questions.
7. **Consider practical implications** — Ask what the findings mean for evaluation, deployment, or decision-making.

Because AI capabilities are changing rapidly, these notes are intended to be **living documents** rather than permanent statements of fact.

## Contents

- `llm-limitations.md` — How rapid frontier-model improvements have changed the traditional picture of LLM limitations
- `ai-evaluation.md` — Why evaluating increasingly capable AI systems requires more than benchmark scores
- `rag-overview.md` — What retrieval-augmented generation solves, what it introduces, and how it should be evaluated
- `llm-hallucinations.md` — How factual reliability has improved while unsupported generation remains a persistent systems problem
- `forecasting-and-model-uncertainty.md` — What weather forecasting teaches us about prediction, uncertainty, calibration, and model error

## A Common Theme

The five notes examine different versions of the same underlying problem:

> **How should we determine whether a system's output deserves our confidence?**

For LLMs, the question appears as:

- Can the model solve the task?
- Does it generalize beyond familiar task distributions?
- Does it know when it is uncertain?
- Can its claims be independently verified?
- Does adding tools or retrieval improve reliability?
- How does performance change as tasks become longer and more complex?

For forecasting, the equivalent question is:

- How accurate is the prediction?
- How well does the forecast represent uncertainty?
- Is the forecast calibrated?
- Does the model capture meaningful signal or merely reduce average error?
- How should users make decisions from probabilistic predictions?

The broader theme is therefore the relationship between:

**Capability → Evidence → Uncertainty → Reliability → Decision**

## Source Standards

Sources are selected using the following hierarchy where practical:

1. Primary research papers and technical reports
2. Official model/system cards and evaluation reports
3. Government and standards organizations
4. Research institutions and operational forecasting centers
5. Peer-reviewed surveys and literature reviews

Vendor-reported benchmark results are treated as useful evidence of measured capability, but not as independent proof of general capability. Where possible, vendor claims are compared with independent evaluations.

## Scope and Limitations

These notes are analytical research summaries, not systematic literature reviews.

The goal is to demonstrate the ability to:

- identify relevant evidence
- compare sources
- recognize methodological limitations
- distinguish observation from inference
- synthesize findings into a defensible conclusion

The notes intentionally avoid pretending that rapidly evolving research has produced final answers where it has not.

**Research status:** Updated August 2026.
