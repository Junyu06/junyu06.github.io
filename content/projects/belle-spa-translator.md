+++
title = "Belle SPA Inc – Internal AI Tools & Automation"
summary = "On-prem LLM system replacing SaaS tools for cost control and internal data privacy."
portfolio_keywords = "On-Prem · Local Deployment · Cost Optimization · Data Privacy · Internal Systems"
weight = -1
+++

**GitHub Repo:** [Junyu06/LLM-Translator](https://github.com/Junyu06/LLM-Translator)

### Demo

![Translator Screenshot](/images/projects/translator.png)


### Problem

Cloud-based SaaS tools for internal workflows incur recurring API costs and raise data privacy concerns for sensitive business operations. Non-technical teams need support for long-form customer inquiries and internal workflows.

### Approach

- Designed and deployed an internal LLM system for long-form inquiries and workflow automation used by non-technical teams
- Implemented schema-constrained generation (Pydantic) with explicit validation boundaries for reliable structured outputs
- Deployed local, on-prem inference on idle hardware to reduce recurring API costs and keep sensitive data off external SaaS tools
- Owned end-to-end delivery (design through deployment) with an emphasis on long-context handling and failure recovery

### Results

- Reduced recurring SaaS/API spend by shifting inference on-prem
- Kept sensitive business data within internal infrastructure by avoiding external SaaS processing
- Delivered predictable, structured outputs for daily internal workflows with failure recovery

### Tech Stack

Python, Pydantic, local LLM deployment, Docker, fault-tolerant pipelines, on-prem inference
