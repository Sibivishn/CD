# Experiment 3: Valid Arithmetic Expression Parser

## Aim
To write a program using LEX and YACC to recognize a valid arithmetic expression containing identifiers, numbers, and operators `+`, `-`, `*`, and `/`.

## Algorithm
1. **Define Tokens (LEX):**
   - Identify valid operands (identifiers starting with a letter/digit combination, or numbers).
   - Match arithmetic operators (`+`, `-`, `*`, `/`, `(`, `)`).
   - Pass tokens to the parser using YACC.
2. **Define Grammar & Precedence (YACC):**
   - Define precedence and associativity rules for arithmetic operators (e.g., `*` and `/` have higher precedence than `+` and `-`).
   - Define context-free grammar rules for valid arithmetic expressions recursively.
   - Handle unary operations like negative numbers (`-expn`).
3. **Parsing & Validation:**
   - Call `yyparse()` in `main()` to evaluate the input expression.
   - If the expression satisfies the grammar rules, display `"valid Expression"`.
   - If a syntax error occurs, trigger `yyerror()` and display `"Invalid Expression"`.

## How to Compile & Run
```bash
lex art_expr.l
yacc -d art_expr.y
gcc lex.yy.c y.tab.c -o art_expr
./art_expr