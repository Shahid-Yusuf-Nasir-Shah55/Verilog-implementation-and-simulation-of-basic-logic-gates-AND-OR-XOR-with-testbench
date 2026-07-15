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




ALU design:-

verilog code:-
// Code your design here
module alu(
    input [7:0] A,
    input [7:0] B,
    input [2:0] Sel,

    output reg [7:0] Result,
    output Zero
);

always @(*) begin

    case(Sel)

        3'b000: Result = A + B;

        3'b001: Result = A - B;

        3'b010: Result = A & B;

        3'b011: Result = A | B;

        3'b100: Result = A ^ B;

        3'b101: Result = ~A;

        3'b110: Result = A << 1;

        3'b111: Result = A >> 1;

        default: Result = 8'b00000000;

    endcase

end

assign Zero = (Result == 8'b00000000);

endmodule


testbench:-

module alu_tb;

reg [7:0] A;
reg [7:0] B;
reg [2:0] Sel;

wire [7:0] Result;
wire Zero;

alu uut(
    .A(A),
    .B(B),
    .Sel(Sel),
    .Result(Result),
    .Zero(Zero)
);

// Waveform generation
initial begin
    $dumpfile("alu.vcd");
    $dumpvars(0, alu_tb);
end

// Test cases
initial begin
    A = 20; B = 10; Sel = 3'b000; #10;
    Sel = 3'b001; #10;
    Sel = 3'b010; #10;
    Sel = 3'b011; #10;
    Sel = 3'b100; #10;
    Sel = 3'b101; #10;
    Sel = 3'b110; #10;
    Sel = 3'b111; #10;
    $finish;
end

endmodule
- Digital Circuit Verification

## Author

Shahid Yusuf Nasir Shah
