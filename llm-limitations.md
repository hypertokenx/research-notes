# LLM Limitations: What Current Evidence Suggests

## Overview

Large language models have become substantially more capable, but their strengths can obscure important limitations. A useful way to understand these limitations is not to ask whether LLMs are "intelligent" or "unintelligent," but to examine where their performance is reliable, where it is fragile, and what conditions cause failures.

Recent research surveys consistently identify reasoning, generalization, hallucination, bias, security, and knowledge limitations as major areas of concern. A 2025 data-driven survey of more than 250,000 ACL and arXiv papers found that reasoning was the most studied limitation, followed by generalization, hallucination, bias, and security. [1]

## 1. Reasoning Is Uneven

LLMs can produce sophisticated-looking solutions while still failing on relatively simple changes in problem structure.

This creates an important distinction between **performance on familiar task distributions** and **robust reasoning ability**. A model may perform extremely well on common benchmark patterns but become less reliable when a problem requires unusual composition, unfamiliar constraints, or systematic adaptation.

This does not mean that LLMs cannot reason. Rather, reasoning ability appears to be highly dependent on task structure, prompting, training, and available tools.

## 2. Knowledge Is Not the Same as Reliable Access to Knowledge

An LLM's parameters contain statistical representations learned during training, but this does not function like a conventional database.

Three problems follow:

* Knowledge can become outdated.
* The model may not reliably retrieve a fact it has encountered.
* The model can generate a plausible answer even when it lacks sufficient evidence.

Retrieval systems, tools, and external sources can partially address these problems, but they introduce their own failure modes.

## 3. Generalization Remains a Major Challenge

Strong benchmark performance does not automatically imply strong performance in every real-world setting.

Real tasks contain distribution shifts, ambiguous instructions, incomplete information, unusual edge cases, and changing environments. Consequently, evaluating a model only on a fixed benchmark can provide an incomplete picture of its reliability.

This is one reason evaluation methodology matters as much as raw benchmark scores.

## 4. Fluency Can Mask Uncertainty

LLMs are optimized to generate useful language, not to provide a calibrated indication of whether every statement is true.

As a result, a response can be:

> fluent + coherent + confident + wrong

This is particularly dangerous because humans tend to use surface quality as a proxy for credibility.

## 5. Tools Change the Failure Profile Rather Than Eliminating It

External tools can give models access to current information, computation, code execution, and retrieval systems.

However, tool use creates additional failure points:

* incorrect tool selection
* incorrect arguments
* poor interpretation of tool output
* failure to verify retrieved information
* manipulation of evaluation environments
* overreliance on retrieved material

The system therefore needs to be evaluated as a **model-plus-tools system**, rather than treating the underlying model as the entire product.

## Synthesis

The common thread across these limitations is that **capability and reliability are different properties**.

A model can be highly capable while remaining unreliable under specific conditions. Benchmark scores measure performance on particular tasks; they do not automatically establish robustness, calibration, or real-world dependability.

This suggests a practical evaluation principle:

> Do not ask only "How well can the model perform?" Ask "Under what conditions does its performance break down?"

That shift moves evaluation from capability demonstration toward reliability assessment.

## Sources

1. Kostikova et al. (2025), *LLLMs: A Data-Driven Survey of Evolving Research on Limitations of Large Language Models*.
2. NIST, *AI Test, Evaluation, Validation and Verification (TEVV)*.
3. NIST, *Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile*.
