# VHDL Counter Overflow Bug

This repository demonstrates a subtle bug in a VHDL counter that involves the improper handling of integer ranges and potential overflow conditions. The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected implementation.

## Bug Description
The original VHDL counter uses an integer type with a defined range. However, it lacks explicit handling for potential overflow situations.  While simulation might show seemingly correct results for some test cases, this could lead to unpredictable behavior in hardware implementations or under different simulation conditions.

## Solution
The `fixed_counter.vhdl` file shows how the bug is addressed by explicitly checking for the upper bound of the integer range before incrementing. This robust solution prevents overflow and ensures predictable counter behavior.

## How to Reproduce
1.  Simulate `buggy_counter.vhdl` and observe the counter behavior when it approaches the upper bound of its range.
2.  Compare the simulation results with those obtained from simulating `fixed_counter.vhdl`. You'll likely find differences indicating the existence of the overflow bug in the original implementation.
