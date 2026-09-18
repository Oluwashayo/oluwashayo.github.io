---
layout: page
title: Authoring evaluation tasks for coding agents
description: SWE-Bench-Pro-style repository evaluation tasks and precision-constrained ML grading harnesses.
img: assets/img/projects/agent_evaluation_tasks.jpg
importance: 6
category: side projects
---

This project focused on designing and authoring rigorous evaluation tasks for autonomous coding agents, benchmarked against real-world, production-grade Python codebases in the style of SWE-Bench-Pro. The objective was creating reproducible failure modes that evaluate an agent's reasoning, debugging, and patch synthesis capabilities.

Each evaluation task comprises an isolated problem description extracted from real issues, gold standard test patches, and strict separation between fail-to-pass (F2P) tests verifying bug resolution and pass-to-pass (P2P) tests preventing functional regression. Custom containerized execution harnesses were built to ensure determinism and eliminate test data leakage.

In addition to software engineering repository tasks, Emmanuel authored a precision-constrained machine learning engineering benchmark for an AI agent evaluation platform, testing autonomous agents on hyperparameter tuning, loss function debugging, and metric optimization under tight computational constraints.

<!-- TODO(shayo) — say which parts you can name publicly -->
