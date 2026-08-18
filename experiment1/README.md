# Experiment 1: Symbol Table Implementation

## Aim
To develop a lexical analyzer using the LEX tool to recognize tokens such as identifiers, constants, comments, and operators in a C program and to create a symbol table while recognizing identifiers.

## Algorithm
1. Start the program by including necessary headers and declarations.
2. Define regular expressions for identifiers, constants, comments, and operators.
3. Create a symbol table data structure.
4. Write rules to insert identifiers into the symbol table if not present.
5. Compile and run with sample C code input.

## Expected Output
```text
Enter your choice
1.Create 2.Insert 3.Modify 4.Search 5.Display 6.Exit: 1
Enter the no. of entries: 3
Enter the variable and the value:
AIM 45
ASK 34
BALL 56

The table after creation is:
VARIABLE    VALUE
AIM         45
ASK         34
BALL        56