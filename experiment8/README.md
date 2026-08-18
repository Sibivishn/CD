# Experiment 8: Type Checking

## Aim
To perform semantic analysis and type checking on variable declarations and assignment expressions using a symbol table.

## Algorithm
1. **Declaration Processing:**
   - Parse declaration statements (e.g., `int a;`).
   - Insert variable names and their data types into the symbol table.
   - Check for duplicate variable declarations.
2. **Expression Type Verification:**
   - Parse assignment expressions of the form `result = op1 operator op2;`.
   - Search for `result`, `op1`, and `op2` in the symbol table to retrieve their declared data types.
3. **Mismatch Detection:**
   - Ensure `op1` and `op2` have compatible types.
   - Ensure the result variable has a data type matching the expression outcome.
   - Print error messages if a type mismatch or undeclared variable is detected.

## Expected Output
```text
IMPLEMENTATION OF TYPE CHECKING

DECLARATIONS (END to finish):
	int a;
	float b;
	int c;
	END

EXPRESSIONS (END to finish):
	a = b + c;
	END

SEMANTIC ANALYZER (TYPE CHECKING):
Type mismatch between operands in 'a = b + c;'