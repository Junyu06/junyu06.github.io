+++
title = "Long-Document LLM Pipeline for Financial Research"
date = "2025-09-01"
+++

**Software Engineer** · Led the LLM component of a large-scale summarization pipeline · Sep 2025 – Dec 2025

### Problem

Long-form documents (10k–20k words) need to be converted into structured outputs for researchers. Raw LLM outputs can be unreliable and cause silent data corruption in downstream systems.

### Approach

- Led the LLM component of a large-scale summarization pipeline that converts long-form documents (10k–20k words) into structured outputs using a MapReduce-style architecture
- Focused on practical system design concerns: semantic chunking, schema-constrained generation (Pydantic), local LLM deployment, and fault-tolerant, resumable workflows
- Designed and implemented idempotent, resumable pipeline stages with self-repair logic, allowing long-running summarization jobs to recover from partial failures without full reprocessing
- Engineered fast-fail validation and explicit failure boundaries, ensuring high-fidelity data extraction that maintains integrity for downstream system consumption

### Results

- Stable processing of 10k–20k word documents with predictable, schema-valid outputs
- Production-grade fault tolerance and recovery for long-running jobs

### Tech Stack

Python, Pydantic, semantic chunking, MapReduce-style pipeline, LLM orchestration, local LLM deployment
