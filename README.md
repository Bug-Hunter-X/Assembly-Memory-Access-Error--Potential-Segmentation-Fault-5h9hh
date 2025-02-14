# Assembly Memory Access Error

This repository demonstrates a common, yet subtle, error in assembly programming: out-of-bounds memory access. The code attempts to access memory using a calculated address, which can lead to a segmentation fault if the calculation results in an invalid address.

The `bug.asm` file contains the erroneous code. The `bugSolution.asm` file provides a corrected version with added bounds checking.

## How to Reproduce

1. Assemble and link the `bug.asm` file.
2. Run the resulting executable.  Under certain conditions (specific values for `ebx` and `ecx`), the program will crash with a segmentation fault.

## Solution

The corrected code in `bugSolution.asm` adds boundary checks before accessing memory to prevent the segmentation fault.  This robust approach ensures the program handles potential out-of-bounds situations gracefully.