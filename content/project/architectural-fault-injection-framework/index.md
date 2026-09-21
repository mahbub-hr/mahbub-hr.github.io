---
title: 'Architectural Fault Injection Framework'
date: '2025-08-01T00:00:00Z'
summary: Register-file and L1 cache fault injection in gem5, plus the automation that ran a 600K-injection campaign in under 24 hours instead of 7 days.

tags:
  - Architecture
  - Systems

# Optional external URL for project (replaces project detail page).
external_link: ''

links:
  - name: Source
    url: https://github.com/mahbub-hr/gem5
    icon_pack: fab
    icon: github

image:
  caption: ''
  focal_point: 'Center'
  preview_only: false
---

You cannot argue about how much a reliability technique helps without measuring how often things actually go wrong. This framework extends the gem5 simulator to inject faults into the register file and the L1 cache, and pinpoints the first instruction that reads corrupted data — at under **0.1% simulation overhead**.

The harder half of the problem is statistical. A single injection tells you nothing; useful confidence intervals need hundreds of thousands of runs. The Python automation layer around gem5 makes that tractable:

- **Checkpointing and parallelism.** Simulations resume from gem5 checkpoints and are distributed across multiple machines. A 600,000-injection campaign across three benchmarks went from **7 days to under 24 hours**.
- **Outcome classification.** Each run is automatically classified as silent data corruption, masked, detected, crash, or timeout, and reported with 99% confidence margins.
- **Root-cause analysis.** When an injection produces a wrong result, the harness diffs execution traces to find where the corrupted value first diverged.

This is the measurement apparatus behind the [AEGIS](../aegis-llvm-compiler-pass-for-hardware-reliability/) numbers.

*Built with C++, Python, gem5, Docker, and Linux.*
