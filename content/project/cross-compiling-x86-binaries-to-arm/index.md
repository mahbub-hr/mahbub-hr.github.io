---
title: 'Cross-Compiling x86 Binaries to ARM'
date: '2024-06-01T00:00:00Z'
summary: Extending the Binrec lifting framework to recompile x86 binaries for AArch64 without source, validated on two real SPEC CPU 2017 programs.

tags:
  - Compilers
  - Architecture

# Optional external URL for project (replaces project detail page).
external_link: ''

links:
  - name: Binrec
    url: https://github.com/trailofbits/binrec-tob
    icon_pack: fab
    icon: github

image:
  caption: ''
  focal_point: 'Center'
  preview_only: false
---

Moving a program to a new instruction set architecture is straightforward when you have the source. When you do not, you have to reconstruct enough of the program's meaning from the binary itself to emit correct code for a different machine.

This project extended [Binrec](https://github.com/trailofbits/binrec-tob) — a dynamic binary lifting framework that recovers LLVM IR by observing concrete executions — to target AArch64 from x86 input. The work centered on two things:

- **Adapting the lifting pipeline.** Binrec's dynamic execution and IR recovery stages assumed an x86 target throughout; retargeting them meant separating what was genuinely architecture-neutral in the recovered IR from what had quietly encoded x86 assumptions.
- **A translation layer for library calls.** Calls out to the C library cross the boundary where the two calling conventions disagree. An x64-to-AArch64 shim translates arguments and return values at that boundary.

The result runs two real-world SPEC CPU 2017 programs, `mcf` and `xalancbmk`, correctly on ARM, at roughly **6× slowdown relative to native**.

A manuscript on the architectural mismatches this work surfaced is in preparation.

*Built with LLVM, C++, S2E, and x86/ARM assembly.*
