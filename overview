# CPU Architecture Overview

This document provides a high-level overview of the pipelined CPU architecture described in this repository.

The design follows a classic **5-stage pipeline** model commonly used to introduce instruction-level parallelism in RISC-style processors. The goal of this architecture is clarity and correctness rather than maximum performance or ISA completeness.

The five pipeline stages are:

1. Instruction Fetch (IF)
2. Instruction Decode (ID)
3. Execute (EX)
4. Memory Access (MEM)
5. Writeback (WB)

Each stage performs a well-defined subset of work and passes results to the next stage via pipeline registers. Control logic and hazard handling mechanisms ensure correct execution in the presence of dependencies and branches.

This documentation focuses on:
- Logical separation of pipeline stages
- Control signal flow
- Hazard detection and resolution strategies
- Architectural tradeoffs
