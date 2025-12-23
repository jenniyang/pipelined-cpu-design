# Performance Tradeoffs

This design intentionally prioritizes simplicity and clarity over maximum throughput.

## Branch Resolution Timing
- Earlier resolution reduces wasted work
- Later resolution simplifies control logic

Resolving branches in the Execute stage represents a balanced compromise.

---

## Forwarding vs. Stalling
- Forwarding improves performance but increases datapath complexity
- Stalling is simpler but reduces instruction throughput

This design implements forwarding for common cases and stalls only when necessary.

---

## Pipeline Depth
- A 5-stage pipeline is easy to reason about
- Deeper pipelines increase complexity and hazard frequency

The chosen depth is well-suited for instructional and documentation purposes.
