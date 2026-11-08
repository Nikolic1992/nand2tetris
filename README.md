# nand2tetris

This repository contains hardware description language (HDL) exercises for
[nand2tetris](https://www.nand2tetris.org/), a course and book about building a
computer from first principles.

## Project 1: Boolean Logic

The chips in [`hardware/projects/01-boolean-logic`](hardware/projects/01-boolean-logic)
implement basic Boolean gates and bus operations using the nand2tetris HDL:

- Boolean gates: `Not`, `And`, `Or`, and `Xor`
- Multiplexers: `Mux`, `Mux16`, `Mux4Way16`, and `Mux8Way16`
- Demultiplexers: `DMux`, `DMux4Way`, and `DMux8Way`
- Bus operations: `Not16`, `And16`, `Or16`, and `Or8Way`

## Project 2: Boolean Arithmetic

The chips in [`hardware/projects/02-boolean-arithmetic`](hardware/projects/02-boolean-arithmetic)
build up arithmetic operations from simple adders to the ALU:

- Adders: `HalfAdder`, `FullAdder`, and 16-bit `Add16`
- Incrementer: `Inc16`
- `ALU`: the 16-bit arithmetic logic unit, which preprocesses the `x` and `y`
  inputs, selects bitwise AND or addition, optionally negates the result, and
  reports the `zr` and `ng` status flags

## Running the chips

Use the nand2tetris Hardware Simulator to open and test the `.hdl` files. The
official project instructions and test files are available from the
[nand2tetris website](https://www.nand2tetris.org/).
