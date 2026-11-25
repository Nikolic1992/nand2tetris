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

## Project 3: Memory

The chips in [`hardware/projects/03-memory`](hardware/projects/03-memory)
implement sequential storage, starting with a 1-bit register and building up
to 16 KB of 16-bit word-addressable memory:

- `Bit`: stores one bit and retains its value when `load` is deasserted
- `Register`: a 16-bit register composed of 16 `Bit` chips
- `RAM8`: 8 16-bit registers, selected by a 3-bit address
- `RAM64`: 64 16-bit registers, organized as eight `RAM8` chips
- `RAM512`: 512 16-bit registers, organized as eight `RAM64` chips
- `RAM4K`: 4,096 16-bit registers, organized as eight `RAM512` chips
- `RAM16K`: 16,384 16-bit registers, organized as four `RAM4K` chips
- `PC`: 16-bit program counter with `reset`, `load`, and `inc` control inputs

Writing is enabled with `load = 1`; the address selects the register or
memory region to update, while `out` exposes the selected value for both reading
and write verification. The program counter gives `reset` highest priority,
followed by `load`, then `inc`; otherwise, it retains its current value.

## Running the chips

Use the nand2tetris Hardware Simulator to open and test the `.hdl` files. The
official project instructions and test files are available from the
[nand2tetris website](https://www.nand2tetris.org/).
