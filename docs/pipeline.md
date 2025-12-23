# Pipeline Design

## Pipeline Stages

### Instruction Fetch (IF)
The IF stage is responsible for:
- Fetching the instruction from instruction memory
- Updating the program counter (PC)
- Handling PC redirection for taken branches

The next PC is typically `PC + 4`, unless overridden by a branch decision from a later stage.

---

### Instruction Decode (ID)
The ID stage:
- Decodes the instruction opcode and fields
- Reads source registers from the register file
- Generates immediate values
- Produces preliminary control signals

This stage also participates in hazard detection by identifying register dependencies with instructions further down the pipeline.

---

### Execute (EX)
The EX stage performs:
- Arithmetic and logical operations
- Branch condition evaluation
- Address calculation for memory operations

Branch decisions are resolved in this stage, balancing simplicity and performance.

---

### Memory Access (MEM)
The MEM stage:
- Reads from data memory for load instructions
- Writes to data memory for store instructions
- Passes ALU results forward for non-memory instructions

---

### Writeback (WB)
The WB stage:
- Writes results back to the register file
- Selects between ALU results and memory data based on instruction type

---

## Pipeline Registers
Pipeline registers separate each stage and store:
- Instruction fields
- Control signals
- Computation results

This separation allows multiple instructions to be in flight simultaneously.
