# Pipelined CPU Architecture — Design Documentation

## Overview

This repository contains **design documentation for a pipelined CPU architecture**, written to demonstrate understanding of **computer architecture concepts** including pipelining, control logic, and hazard handling.

The documentation is based on an independently written design inspired by coursework in **computer architecture**, and is intended for **learning and portfolio purposes**. No course starter code, solutions, or autograder materials are included.

---

## What’s Inside

- Clear explanations of a **5-stage pipeline** (IF, ID, EX, MEM, WB)
- Control signal generation and propagation
- Data and control hazard handling strategies
- Performance tradeoffs and design limitations
- Diagrams illustrating pipeline flow and forwarding paths

---

## Architecture Summary

The CPU follows a classic 5-stage pipeline model:

1. **Instruction Fetch (IF)**
2. **Instruction Decode (ID)**
3. **Execute (EX)**
4. **Memory Access (MEM)**
5. **Writeback (WB)**

Each stage is separated by pipeline registers, and control logic coordinates instruction flow and hazard resolution.

See `docs/pipeline.md` and `diagrams/pipeline_diagram.png` for details.

---

## Hazard Handling

### Data Hazards
- Forwarding from later pipeline stages when possible
- Stall insertion when forwarding cannot resolve dependencies

### Control Hazards
- Branch resolution in the Execute stage
- Pipeline flush on taken branches

Design rationale and alternatives are discussed in `docs/hazard_handling.md`.

---

## Performance Tradeoffs

Key tradeoffs explored include:

- Early vs. late branch resolution
- Forwarding complexity vs. stall frequency
- Simplicity vs. maximum throughput

See `docs/performance_tradeoffs.md`.

---

## Disclaimer

This repository is **documentation-only** and does **not** contain source code from any course assignment.  
All content is independently written and intended to demonstrate conceptual understanding rather than provide an implementation.

---

## Why This Matters

This documentation demonstrates:

- Systems-level reasoning
- Ability to clearly explain complex technical designs
- Familiarity with CPU pipelines and hazard management
- Strong technical communication skills

---

## Background

Inspired by coursework in computer architecture at UC Berkeley.

---

## 📄 Suggested Resume Line

**CPU Architecture Design Documentation** — Authored detailed design docs for a 5-stage pipelined CPU, including hazard handling, control logic, and performance tradeoffs.
