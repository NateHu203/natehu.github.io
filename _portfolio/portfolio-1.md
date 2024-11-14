---
title: "Paper Review: ADaPT: Dynamic Task Decomposition for Language Models"
excerpt: "A deep dive into ADaPT's innovative approach to task planning and decomposition with LLMs"
header:
  teaser: images/adapt_flow.png
  image: images/adapt_flow.png
collection: portfolio
permalink: /portfolio/adapt-paper-review/
---

## Paper Overview
[ADaPT: As-Needed Decomposition and Planning with Language Models](https://arxiv.org/abs/2311.0577) introduces an elegant solution to one of the key challenges in LLM task execution: knowing when and how to break down complex tasks. Unlike traditional approaches that either decompose everything or nothing, ADaPT takes a more nuanced, human-like approach.

## Key Innovations

### 1. Recursive Decision Making
ADaPT's core strength lies in its recursive algorithm that makes dynamic decisions about task decomposition:
- First attempts direct execution
- Only decomposes tasks when execution fails
- Uses binary success heuristics for clear decision-making

### 2. Dual LLM Roles
The system cleverly splits responsibilities between:
- **Executor LLM**: Handles direct task execution through environment interaction
- **Planner LLM**: Decomposes complex tasks into 3-5 manageable high-level steps

### 3. Smart Decomposition Strategy
- Maintains high-level initial decompositions
- Uses dmax+1 constraint to ensure sufficient task completion
- Implements AND-OR compositional logic for task relationships

## Why It Matters
Traditional task planning faces several challenges:
- Over-decomposition of simple tasks wastes resources
- Under-decomposition of complex tasks leads to failures
- Fixed decomposition strategies lack flexibility

ADaPT addresses these by:
- Decomposing only when necessary
- Maintaining efficiency for simple tasks
- Ensuring complex tasks get appropriate attention
