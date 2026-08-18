## Experiment 4: Valid Variable Recognition

### `CompilerDesign_experiments/experiment4/README.md`
```markdown
# Experiment 4: Valid Variable Recognition

## Aim
To write a program using LEX and YACC to recognize a valid C variable name starting with a letter followed by any number of letters or digits.

## Algorithm
1. **Lexical Analysis (LEX):**
   - Define patterns to match letters (`[a-zA-Z]`) and digits (`[0-9]`).
   - Return corresponding tokens `LET` and `DIG` to the YACC parser.
2. **Syntax Analysis (YACC):**
   - Define non-terminal `var` using grammar rules:
     - `var -> LET`
     - `var -> var LET`
     - `var -> var DIG`
   - This ensures the variable name **must** start with a letter.
3. **Parsing:**
   - Call `yyparse()` to evaluate user input.
   - Print `"Valid variable"` on successful match.
   - Print `"Invalid variable"` if the syntax rule is violated (e.g., starting with a digit).

## How to Compile & Run
```bash
lex valvar.l
yacc -d valvar.y
gcc lex.yy.c y.tab.c -o valvar
./valvar