Enter Three Address Code (end with CTRL+Z on Windows or CTRL+D on Linux):
a=2+4;
b=d*1;
c=s*2;
^Z

Terminal Output:
Unoptimized Code:
a=2+4;
b=d*1;
c=s*2;

Optimized Code:
a=6;	// Constant Folding
b=d;	// Algebraic Simplification (X*1 or X/1)
c=s+s;	// Strength Reduction (X*2 to X+X)