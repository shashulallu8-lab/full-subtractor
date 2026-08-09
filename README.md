# Full Subtractor using Verilog HDL

## Project Overview

A Full Subtractor is a combinational logic circuit that subtracts three binary inputs:

- A (Minuend)
- B (Subtrahend)
- Bin (Borrow Input)

It produces two outputs:

- Difference (D)
- Borrow Out (Bout)

---

## Truth Table

| A | B | Bin | Difference | Borrow |
|---|---|-----|------------|---------|
|0|0|0|0|0|
|0|0|1|1|1|
|0|1|0|1|1|
|0|1|1|0|1|
|1|0|0|1|0|
|1|0|1|0|0|
|1|1|0|0|0|
|1|1|1|1|1|

---

## Boolean Expressions

Difference = A ⊕ B ⊕ Bin

Borrow = (~A & B) | (~A & Bin) | (B & Bin)

---

## Files Included

- full_subtractor.v
- full_subtractor_tb.v
- waveform.png
- simulation_output.txt

---

## Software Used

- Xilinx Vivado
- ModelSim
- Icarus Verilog
- GTKWave

---

## How to Run

Compile

```
iverilog -o full_subtractor full_subtractor.v full_subtractor_tb.v
```

Run

```
vvp full_subtractor
```

Generate waveform

```
gtkwave full_subtractor.vcd
```

---

## Expected Output

```
A B Bin | Diff Borrow

0 0 0 | 0 0
0 0 1 | 1 1
0 1 0 | 1 1
0 1 1 | 0 1
1 0 0 | 1 0
1 0 1 | 0 0
1 1 0 | 0 0
1 1 1 | 1 1
```

---

## Author

Your Name
