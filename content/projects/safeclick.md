+++
title = "SafeClick – Phishing Detection System"
summary = "Multi-stage URL analysis with constrained LLM reasoning and deterministic risk scoring."
portfolio_keywords = "Security AI · Multi-stage Pipelines · Production Design"
+++

### Problem

Traditional ML or LLM-only approaches fail in phishing detection due to sparse signals, zero-day variants, and unreliable external evidence. Users need a security-focused system that operates under real-world constraints.

### Approach

- Designed a multi-stage phishing detection pipeline for URLs with constrained LLM reasoning and deterministic risk scoring
- Treated the LLM as a probabilistic component behind explicit validation boundaries, caching/deduplication, and fallback logic
- Engineered for reliability under degraded dependencies with clear failure modes and cost control
- Evolved a hackathon prototype toward a production-ready security service with system boundaries and observability

### Results

- Won 1st Place and Most Secure Project Award (Hofstra-Pensar Hackathon)
- Reduced nondeterminism in decision outputs through deterministic scoring and validation boundaries
- Improved resilience to partial failures via explicit fallbacks and pipeline-stage fault handling

### Tech Stack

Python, Pydantic, LLM orchestration, multi-stage URL analysis, caching, deduplication
