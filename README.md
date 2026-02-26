# CodingAgency

CodingAgency is an AI-native software production pipeline.

It transforms a single `PRD.md` into a generated, reviewed, executed,
debugged, deployed, and documented system through deterministic,
stage-isolated LLM agents.

The architecture enforces strict cognitive separation between phases.
Each agent operates under constrained responsibility, minimizing drift,
token waste, and cross-stage contamination.

All prompts were engineered, iterated, validated, and stress-tested
exclusively with **Gemini 3.1 Pro**.  
However, the framework is fully model-agnostic and designed to remain
robust across frontier and mid-tier LLMs.

---

# Architectural Principles

### 1. Deterministic Stage Isolation
Planning, validation, implementation, debugging, deployment, and
documentation are separated into independent execution phases.
No stage overlaps responsibility.

### 2. Token Density Optimization
Prompts are structured to maximize signal per token:
- No conversational overhead
- Minimal verbosity
- Structured output enforcement
- Explicit execution directives

### 3. PRD as Single Source of Truth
All architectural and implementation decisions derive strictly from
`PRD.md`. No implicit assumptions override defined requirements.

### 4. Model-Strength Alignment
Different phases require different cognitive capabilities.
Model selection should match task type — not raw model size.

---

# Model Alignment Strategy

## START — Planning & Scaffolding  
Structured reasoning model recommended  
(e.g., GPT-4.1, Claude Sonnet, Gemini 1.5 Pro)

## REVIEW — Architectural Validation  
High analytical reasoning model recommended  
(e.g., Claude Sonnet, GPT-4.1)

## EXECUTE — Code Generation  
Strong coding model required  
(e.g., Claude Sonnet, GPT-4.1)  
Frontier-tier models only for large or complex systems.

## DEBUG — Logical Resolution  
Multi-step reasoning model recommended  
(e.g., Claude Sonnet, GPT-4.1)

## DEPLOY — Infrastructure Execution  
Structured reasoning model sufficient  
(e.g., GPT-4.1, Claude Sonnet)

## DOCUMENT — Structured Summarization  
Efficient structured model sufficient  
(e.g., GPT-4.1-mini, Gemini Flash)

---

CodingAgency is not a prompt collection.

It is a staged cognitive architecture for AI-driven software production.
