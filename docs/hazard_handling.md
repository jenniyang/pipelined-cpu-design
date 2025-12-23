# Hazard Handling

Pipelined execution introduces hazards that must be resolved to ensure correct program behavior.

---

## Data Hazards

### Forwarding
When possible, results are forwarded from later pipeline stages to earlier ones to avoid unnecessary stalls.

Examples include:
- EX/MEM to EX forwarding
- MEM/WB to EX forwarding

### Stalling
If forwarding cannot resolve a dependency (e.g., a load-use hazard), the pipeline inserts a stall by:
- Pausing PC and IF/ID register updates
- Inserting a bubble into the pipeline

---

## Control Hazards

Branches introduce uncertainty in control flow.

### Resolution Strategy
- Branch conditions are evaluated in the Execute stage
- If a branch is taken, incorrect-path instructions are flushed

This approach simplifies the design at the cost of a small performance penalty.

---

## Tradeoffs
- More aggressive branch prediction improves performance but increases complexity
- Simple flushing is easier to reason about and verify
