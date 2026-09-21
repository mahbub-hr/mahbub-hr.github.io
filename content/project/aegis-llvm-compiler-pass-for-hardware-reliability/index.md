---
title: 'AEGIS: An LLVM Pass for Hardware Reliability'
date: '2025-08-01T00:00:00Z'
summary: An LLVM transformation pass that duplicates computation and checks it before stores, branches, and calls, cutting silent data corruption by up to 29× under cache fault injection.

tags:
  - Compilers
  - Architecture

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: ''
  focal_point: 'Center'
  preview_only: false
---

Transient hardware faults — a bit flipped in a cache line or a register by a stray particle or a marginal voltage — do not announce themselves. The machine keeps running and quietly produces the wrong answer. AEGIS is an LLVM pass that makes a program check its own arithmetic, so that a corrupted value is caught before it can escape.

The pass implements **Error Detection by Duplicated Instructions (EDDI)**. It duplicates global, stack, and heap values and compares the two copies at the points where a wrong value would become observable: before a store, before a branch, and before a function call. Getting this to work on real programs meant more than duplicating instructions:

- **Call boundaries.** Call sites are rewritten to pass shadow arguments and retrieve shadow return values, so duplication survives across function calls rather than stopping at each one.
- **Pointer sizes.** Knowing how much memory to duplicate behind a pointer is not something the IR tells you. The pass recovers it from DWARF debug metadata, falling back to a signature table for library calls.
- **Extensibility.** Hardening schemes are registered through a strategy registry, so adding a new one is a single self-registering file rather than an edit threaded through the pass.
- **Testing.** A regression suite validates both that the transformation is correct and that fault-detection coverage holds across the benchmark suite.

Measured against L1 cache fault injection, AEGIS reduces silent data corruption by **1.3× to 29×** across `qsort`, `matmul`, and `CRC32`, at a runtime cost of 1.6× to 3.0×.

*Built with C++, LLVM, Clang, and CMake.*
