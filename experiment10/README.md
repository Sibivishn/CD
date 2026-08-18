# Experiment 10: Compiler Back-End (8086 Code Generation)

## Aim
To write a compiler back-end program that converts Three-Address Code (TAC) into target 8086 assembly language instructions.

## Algorithm
1. **Input Parsing:**
   - Read Three-Address Code instructions line by line.
   - Parse into target variable, operand 1, operator, and operand 2.
2. **Instruction Translation:**
   - Load operand 1 into register `AX`: `MOV AX, op1`
   - Map operators to 8086 instructions:
     - `+` $\rightarrow$ `ADD AX, op2`
     - `-` $\rightarrow$ `SUB AX, op2`
     - `*` $\rightarrow$ `MUL op2`
     - `/` $\rightarrow$ `MOV DX, 0` $\rightarrow$ `MOV BX, op2` $\rightarrow$ `DIV BX`
   - Move result back to memory: `MOV result, AX`
3. **Simple Assignment Handling:**
   - If the line is an assignment without operators (`x = t1`), output `MOV AX, t1` followed by `MOV x, AX`.

## Expected Output
```text
Enter number of three-address code lines: 3
Enter the three-address code:
t1 = a + b
t2 = t1 * c
x = t2

Generated 8086 Assembly Code:

MOV AX, a
ADD AX, b
MOV t1, AX

MOV AX, t1
MUL c
MOV t2, AX

MOV AX, t2
MOV x, AX