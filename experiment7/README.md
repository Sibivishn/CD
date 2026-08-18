# Experiment 7: Three-Address Code Generation

## Aim
To generate Three-Address Code (TAC) intermediate representations for a given arithmetic assignment statement using LEX and YACC.

## Algorithm
1. **Lexical Analysis (LEX):**
   - Recognize identifiers (`ID`) and numbers (`NUM`).
   - Duplicate string values into `yylval.str` and pass to YACC.
2. **Intermediate Representation Rules (YACC):**
   - Define string-based stack values for non-terminals.
   - For every binary operation (`+`, `-`, `*`, `/`), generate a new temporary variable name (`t1`, `t2`, etc.).
   - Print three-address instructions (e.g., `t1 = b * c`).
   - Pass the temporary variable string up the evaluation tree.
3. **Final Assignment:**
   - Print the final assignment statement (e.g., `x = t3`).

## How to Compile & Run
```bash
lex tac.l
yacc -d tac.y
gcc y.tab.c lex.yy.c -o tac
./tac