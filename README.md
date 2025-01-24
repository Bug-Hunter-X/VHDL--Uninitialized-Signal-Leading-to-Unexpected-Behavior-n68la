# VHDL Uninitialized Signal Bug

This repository demonstrates a common error in VHDL: using an uninitialized signal.  Uninitialized signals can lead to unpredictable behavior and make debugging difficult.  The `bug.vhdl` file contains the erroneous code, while `bugSolution.vhdl` provides the corrected version.

## Problem

The `internal_data` signal in `bug.vhdl` is declared but not given an initial value. This means its initial state is undefined, resulting in an unpredictable output on the first clock cycle.  The value of `data_out` will be whatever random value happens to be present in the memory location allocated to `internal_data`.

## Solution

The `bugSolution.vhdl` file corrects the issue by explicitly initializing `internal_data` to a known value (in this case, "00"). This ensures that the output is predictable and consistent from the start.

## Lessons Learned

Always initialize your signals in VHDL to prevent unexpected behavior and ensure reliable simulation and synthesis results.