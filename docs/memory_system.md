# Memory System

The architecture assumes a simplified memory model suitable for instructional purposes.

## Instruction Memory
- Read-only
- Accessed during the IF stage
- One instruction fetched per cycle

## Data Memory
- Accessed during the MEM stage
- Supports load and store operations
- Assumed to have a single-cycle latency

## Design Assumptions
- No caches are modeled
- Memory is always available
- Structural hazards are avoided through design constraints

These assumptions allow the design to focus on pipeline behavior rather than memory hierarchy complexity.
