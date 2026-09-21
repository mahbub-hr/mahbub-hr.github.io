---
title: 'IR-Sentinel: LLVM-IR Security Analysis via MCP'
date: '2026-02-01T00:00:00Z'
summary: A Model Context Protocol server that exposes a local LLVM toolchain to an AI agent, which compiles C++ to IR and hunts for use-after-free patterns.

tags:
  - Compilers
  - Systems

# Optional external URL for project (replaces project detail page).
external_link: ''

links:
  - name: Source
    url: https://github.com/mahbub-hr/ir-sentinel
    icon_pack: fab
    icon: github

image:
  caption: ''
  focal_point: 'Center'
  preview_only: false
---

Language models are good at recognizing patterns in code and bad at knowing what the compiler actually did with it. IR-Sentinel is a proof of concept that closes that gap by handing the model the compiler.

It is a **Model Context Protocol (MCP)** server, built on `FastMCP`, that exposes a local LLVM toolchain — `clang` and `opt` — as tools an AI agent can call. The agent pipeline then:

1. Compiles C++ source to **LLVM IR**,
2. Extracts **control flow graph** metrics from it,
3. Iteratively queries **Gemini** against that structured view to identify use-after-free vulnerability patterns.

The interesting part is that the model reasons over the IR and the CFG rather than over surface syntax, so it sees the program the way the optimizer does.

*Built with Python, LLVM, Gemini, and FastMCP.*
