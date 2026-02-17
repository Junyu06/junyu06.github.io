+++
title = "Transcriptor"
summary = "Artifact-based transcription pipeline with resumable job tracking and deterministic outputs."
portfolio_keywords = "Workflow Design · Stateful Workflows · Job Persistence · Reliability"
weight = -2
+++

### Problem

Audio and video content needs to be converted into searchable, reliable text artifacts for accessibility and downstream indexing. Naive transcription runs often fail mid-job or produce inconsistent outputs that are difficult to validate and resume.

### Approach

- Designed an artifact-based transcription pipeline that treats intermediate outputs as first-class build products
- Implemented resumable job tracking with explicit stage boundaries to recover from partial failures without restarting
- Engineered deterministic, repeatable outputs to support downstream indexing and automated post-processing
- Added validation and guardrails around stage transitions to prevent silent corruption in stored artifacts

### Results

- Produced consistent, deterministic transcription artifacts suitable for indexing and search
- Eliminated full-job reprocessing by resuming from the latest valid artifact boundary after failures
- Maintained predictable processing behavior across long-running transcription workloads

### Tech Stack

Artifact-based pipeline, resumable job tracking, deterministic outputs, validation boundaries
