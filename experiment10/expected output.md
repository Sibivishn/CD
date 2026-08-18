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