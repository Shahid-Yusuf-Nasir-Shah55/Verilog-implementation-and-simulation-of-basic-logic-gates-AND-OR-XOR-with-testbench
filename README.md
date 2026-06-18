# Verilog-implementation-and-simulation-of-basic-logic-gates-AND-OR-XOR-with-testbench
Verilog implementation and simulation of basic logic gates (AND, OR, XOR) with testbenches and waveform verification using Icarus Verilog and EPWave.
# Logic Gates Using Verilog

This repository contains the Verilog implementation, testbench, and waveform verification of basic logic gates.

## Gates Implemented

1. AND Gate
2. OR Gate
3. XOR Gate

## Tools Used

- Verilog HDL
- EDA Playground
- Icarus Verilog
- EPWave

---

## AND Gate

### Verilog Code

```verilog
module and_gate(
    input A,
    input B,
    output Y
);

assign Y = A & B;

endmodule
```

### Truth Table

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

### Waveform

Insert screenshot: `AND_Gate/waveform.png`

---

## OR Gate

### Verilog Code

```verilog
module or_gate(
    input A,
    input B,
    output Y
);

assign Y = A | B;

endmodule
```

### Truth Table

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

### Waveform

Insert screenshot: `OR_Gate/waveform.png`

---

## XOR Gate

### Verilog Code

```verilog
module xor_gate(
    input A,
    input B,
    output Y
);

assign Y = A ^ B;

endmodule
```

### Truth Table

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### Waveform

Insert screenshot: `XOR_Gate/waveform.png`

---

## Simulation

The circuits were verified using custom testbenches and waveform analysis.

### Test Cases

```text
A=0 B=0
A=0 B=1
A=1 B=0
A=1 B=1
```

### Verification

The simulation results matched the expected truth tables for all gates.

---

## Learning Outcomes

- Verilog HDL Basics
- Combinational Logic Design
- Testbench Development
- Waveform Analysis
- Digital Circuit Verification

## Author

Shahid Yusuf Nasir Shah
