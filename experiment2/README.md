# Experiment 2: Lexical Analyzer

## Aim
To implement a lexical analyzer that reads C source code and identifies individual tokens (keywords, identifiers, operators, delimiters, header files, preprocessor directives).

## Algorithm
1. Define token patterns.
2. Read the source code character by character or token by token.
3. Identify and classify tokens.
4. Output token classification.

## Expected Output
```text
Enter filename : iplex.c
Delimitter #
Preprocessor directive include
Delimitter <
Header file stdio.h
Delimitter >
Keyword void
Identifier main
End of file