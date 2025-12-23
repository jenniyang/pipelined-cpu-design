# Control Logic

The control unit is responsible for generating signals that coordinate data movement and operations throughout the pipeline.

## Control Signals
Typical control signals include:
- ALU operation selection
- Register write enable
- Memory read/write enable
- Writeback source selection
- Branch control flags

## Control Propagation
Control signals are generated during the Decode stage and propagated through the pipeline alongside data values. This ensures that each instruction carries the information needed to behave correctly in later stages.

## Design Considerations
- Centralized control simplifies reasoning
- Clear signal naming improves debuggability
- Control signals must be flushed or nulled on incorrect-path instructions
