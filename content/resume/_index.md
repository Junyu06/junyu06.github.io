+++
title = "Resume"
+++

{{< download_button text="Download Resume" href="/Junyu%20Li%20Resume.pdf" >}}

## Professional Summary

Lead Software Engineer specializing in LLM orchestration and production AI systems.  
Experience building deterministic multi-stage workflows with validation and failure recovery.  
Focused on reliability, cost optimization, and end-to-end ownership from prototype to production.

## Experience (Condensed)

### SafeClick - Lead Software Engineer

- Led a 5-engineer team to evolve SafeClick from hackathon prototype into a production phishing-detection service.
- Built a deterministic security logic layer over probabilistic LLM outputs to improve reliability under sparse, zero-day signals.
- Designed URL structure analysis -> sandbox evidence -> final verdict pipeline with explicit validation and safe fallbacks.

### Belle SPA Inc - Applied AI Engineer

- Architected and deployed an on-prem LLM system replacing SaaS tools, reducing recurring API costs and improving data control.
- Built schema-constrained pipelines with Pydantic for deterministic structured outputs in internal AI workflows.
- Optimized inference performance and production reliability across long-running internal workflows.

## Selected Projects

### LLM Pipeline - Long-document summarization

- Implemented MapReduce-style orchestration for 20k-word inputs with bounded context.
- Engineered idempotent and resumable stages for robust partial-failure recovery.
- Enforced Pydantic schema validation to prevent silent corruption in downstream workflows.

### Transcriptor - Artifact-based workflow system

- Designed stateful artifact boundaries for deterministic transcription outputs.
- Added resumable stage transitions to avoid full-job reruns after failures.

## Education

### Hofstra University

- Master of Science in Computer Science, Jan 2025 - Dec 2025, **GPA 4.0 / 4.0**
- Bachelor of Science in Computer Science, Sep 2022 - May 2025, **GPA 3.8 / 4.0**

## Skills

- **Languages:** Python · TypeScript · SQL · C++
- **AI Systems:** LLM Orchestration · Validation Layers · Workflow Design
- **Infrastructure:** Docker · Local Inference · REST APIs

## Honors

1st Place Hackathon · Most Secure Project Award · Provost's Scholars · Dean's List
