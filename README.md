# CSE345 — Digital Logic Design

Coursework for **CSE 345 – Digital Logic Design** (Spring 2026, Section 2):
the lab assignment and the final lab project on combinational-circuit design.

---

## Contents

| File | Description |
|---|---|
| `Assignment.pdf` | Lab assignment specification. |
| `CSE345 Lab Report(Final).pdf` | Final lab project report. |

---

## Final project — 2-Bit Full Adder using Multiplexers

**Title:** *Design and Implementation of a 2-Bit Full Adder Circuit using Multiplexers*

A **full adder** is a combinational logic circuit that performs binary addition.
In this project a **2-bit full adder** is designed with the **cascade method**:
two 1-bit full adders are connected in series, and the carry-out of the first stage
is fed as the carry-in of the second stage — removing the need for an external carry
input.

The circuit takes two 2-bit numbers **(A1 A0)** and **(B1 B0)** and produces
**Sum1**, **Sum2**, and a final **carry-out**.

### Design approach

Rather than using only basic gates, the outputs are implemented with
**multiplexers**, following the truth tables of each output:

- **8:1 multiplexer** → generates **Sum1**
- **2:1 multiplexers** → generate **Sum2** and the carry function
- **AND / OR gates** → final carry generation (`Cfinal`)

Input variables act as the multiplexer **select lines**, and the data inputs
(I0–I7) are assigned according to the derived truth tables. The cascade structure
propagates the carry from the LSB stage to the MSB stage, completing the 2-bit
addition.

### Workflow

1. Build the full truth table for 2-bit addition and derive separate truth tables
   for **Sum1**, **Sum2**, and **Carry**.
2. Reduce each output to Boolean form and map it onto multiplexer inputs.
3. Implement the circuit using the cascade method and arrange the select lines
   and data inputs.
4. Simulate the design, apply all input combinations, and verify the outputs
   against the truth table.
5. Compare simulation results with the expected values.

### Components used

- 8:1 multiplexer IC
- 2:1 multiplexer ICs
- 4-input AND / OR ICs
- 2-input OR IC
- Breadboard, wires, trainer board

### Result

The simulated outputs matched the expected truth-table values for all input
combinations, confirming the correctness of the multiplexer-based cascaded design.

---

## Course info

- **Course:** CSE 345 — Digital Logic Design
- **Section:** 2
- **Instructor:** Dr. Md Sawkat Ali (Associate Professor, Dept. of CSE)
- **Submitted by:** Inteshar Alam, Ratul Hasan Nirjon
- **Submission date:** 23 April 2026
