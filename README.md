# VHDL Integer Overflow Bug
This repository demonstrates a common error in VHDL code: integer overflow in a counter. The `buggy_counter.vhdl` file contains the erroneous code, while `fixed_counter.vhdl` provides a corrected version.  The bug arises from incrementing the counter *before* checking for the maximum value. This can lead to unpredictable behavior if the maximum value is reached.

## How to Reproduce
1. Synthesize and simulate `buggy_counter.vhdl`. 
2. Observe the counter's behavior when it reaches its maximum value (15).  You'll notice it briefly goes out of range before resetting.
3. Synthesize and simulate `fixed_counter.vhdl` for comparison.  The corrected code prevents the overflow.

## Solution
The issue is resolved by checking if the counter has reached its maximum value *before* incrementing it.  The corrected code ensures that the overflow condition is handled correctly, preventing unexpected behavior.