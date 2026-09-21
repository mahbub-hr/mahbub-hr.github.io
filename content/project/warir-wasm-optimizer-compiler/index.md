---
title: 'WARIR: A WebAssembly Optimizing Compiler'
date: '2024-06-01T00:00:00Z'
summary: A full SMPL-to-WebAssembly compiler with graph-coloring register allocation and SSA-based dataflow optimization.

tags:
  - Compilers

# Optional external URL for project (replaces project detail page).
external_link: ''

links:
  - name: Source
    url: https://github.com/mahbub-hr/compiler_cs241/tree/main/Project3
    icon_pack: fab
    icon: github

image:
  caption: ''
  focal_point: 'Center'
  preview_only: false
---

A complete compiler pipeline from the SMPL teaching language down to WebAssembly, written for a graduate compilers course.

The back end is where most of the work went:

- **Graph-coloring register allocation**, building the interference graph from live ranges and spilling when the graph is not colorable with the available registers.
- **SSA-based dataflow analysis** driving common subexpression elimination and copy propagation, with the optimizations expressed as transformations on the SSA form rather than ad-hoc peephole rules.

*Built with Python, Node.js, and WebAssembly.*
