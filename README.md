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

## Running the chips

Use the nand2tetris Hardware Simulator to open and test the `.hdl` files. The
official Project 1 instructions and test files are available from the
[nand2tetris website](https://www.nand2tetris.org/project01).
