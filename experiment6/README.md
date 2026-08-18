# Experiment 6: Calculator Using LEX and YACC

## Aim
To implement a simple arithmetic calculator capable of evaluating addition, subtraction, multiplication, and division expressions using LEX and YACC.

## Algorithm
1. **Tokenization (LEX):**
   - Tokenize sequences of digits as floating-point numbers (`NUM`) and return `atof(yytext)` in `yylval`.
   - Pass operators (`+`, `-`, `*`, `/`) and parentheses directly to YACC.
2. **Expression Evaluation (YACC):**
   - Set operator precedence (`*`, `/` higher than `+`, `-`).
   - Define recursive expression rules (`E`):
     - `E -> E + E { $$ = $1 + $3; }`
     - `E -> E - E { $$ = $1 - $3; }`
     - `E -> E * E { $$ = $1 * $3; }`
     - `E -> E / E { $$ = $1 / $3; }`
3. **Execution:**
   - Execute calculations during parsing using embedded action code and display the result (`Answer: %g`).

## How to Compile & Run
```bash
lex cal.l
yacc -d cal.y
gcc lex.yy.c y.tab.c -o calc
./calc