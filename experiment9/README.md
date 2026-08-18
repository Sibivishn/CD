# Experiment 9: Code Optimization Techniques

## Aim
To implement basic machine-independent code optimization techniques including Constant Folding, Strength Reduction, and Algebraic Simplification on Three-Address Code.

## Algorithm
1. **Input Reading:**
   - Read Three-Address Code lines from standard input and save to a temporary file/array.
2. **Pattern Matching & Optimization Checks:**
   - **Constant Folding:** If both operands are constants (e.g., `2 + 4`), compute the value at compile time (`6`).
   - **Algebraic Simplification:** If multiplying/dividing by 1 (e.g., `d * 1`), eliminate the operation (`d`).
   - **Strength Reduction:** Replace expensive operations with cheaper ones (e.g., convert `s * 2` to `s + s`).
3. **Output:**
   - Print the optimized Three-Address Code along with annotations detailing which technique was applied.

## Expected Output
```text
Unoptimized Code:
a=2+4;
b=d*1;
c=s*2;

Optimized Code:
a=6;	// Constant Folding
b=d;	// Algebraic Simplification (X*1 or X/1)
c=s+s;	// Strength Reduction (X*2 to X+X)