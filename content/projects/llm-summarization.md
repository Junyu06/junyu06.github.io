+++
title = "Long-Document LLM Pipeline for Financial Research"
summary = "MapReduce-style orchestration for 20k-word inputs with schema validation and failure recovery. Demonstrates complex data workflow and architecture skills."
portfolio_keywords = "LLM Orchestration · MapReduce · Schema Validation · Reliability"
weight = 0
+++

### Problem

Long-form documents (10k–20k words) need to be converted into structured outputs for researchers. Raw LLM outputs can be unreliable and cause silent data corruption in downstream systems.

### Approach

- Designed a MapReduce-style LLM orchestration pipeline for 10k-20k word inputs
- Implemented schema-constrained generation with Pydantic and explicit validation boundaries
- Engineered idempotent, resumable stages with self-repair logic for partial-failure recovery
- Deployed local LLM inference to control cost and data flow

### Results

- Consistently produced schema-valid structured outputs across long-context inputs
- Eliminated full-job reprocessing through stage-level recovery design
- Maintained predictable processing behavior across long-running workloads

### Tech Stack

Python, Pydantic, semantic chunking, MapReduce-style pipeline, LLM orchestration, local LLM deployment
