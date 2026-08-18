
# Experiment 5: Recognition of C Control Structures Syntax

## Aim
To write a program using LEX and YACC to recognize valid control structure syntax in the C language (such as `if-else`, `while`, `for`, and `switch-case`).

## Algorithm
1. **Lexical Analysis (LEX):**
   - Define patterns for keywords (`if`, `else`, `while`, `for`, `switch`, `case`, `default`).
   - Define patterns for identifiers, numbers, delimiters (`{`, `}`, `(`, `)`, `;`), and relational operators (`==`, `<=`, `>=`, `<`, `>`).
2. **Grammar Definition (YACC):**
   - Construct production rules for C statements:
     - `if_stmt -> IF ( cond ) stmt | IF ( cond ) stmt ELSE stmt`
     - `while_stmt -> WHILE ( cond ) stmt`
     - `for_stmt -> FOR ( ID = NUM ; cond ; ID = ID ) stmt`
     - `switch_stmt -> SWITCH ( ID ) { case_list }`
3. **Evaluation:**
   - Parse input using `yyparse()`.
   - If the sequence matches the grammar rules, print `"Valid control structure syntax."`
   - If parsing fails, output `"Invalid control structure syntax."`

## How to Compile & Run
```bash
lex control.l
yacc -d control.y
gcc lex.yy.c y.tab.c -o control
./control