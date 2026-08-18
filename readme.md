# CS4501 - Compiler Design Lab Experiments

This repository contains the complete set of source codes, Lex/Yacc definitions, algorithms, and documentation for the **CS4501 - Compiler Design** laboratory course.

---

## Directory Structure

```text
CompilerDesign_experiments/
├── experiment1/   # Symbol Table Implementation (C)
├── experiment2/   # Lexical Analyzer in C
├── experiment3/   # Valid Arithmetic Expression Parser (LEX & YACC)
├── experiment4/   # Valid Variable Recognition (LEX & YACC)
├── experiment5/   # C Control Structures Syntax Recognition (LEX & YACC)
├── experiment6/   # Calculator Implementation (LEX & YACC)
├── experiment7/   # Three-Address Code (TAC) Generation (LEX & YACC)
├── experiment8/   # Type Checking Implementation (C)
├── experiment9/   # Code Optimization Techniques (C)
└── experiment10/  # Compiler Back-End: 8086 Code Generation (C)
```

---

## Experiments

### 1. Symbol Table Implementation
- **Tools / Languages:** C
- **Key Concepts:** Symbol creation, search, insert, and modification

### 2. Lexical Analyzer
- **Tools / Languages:** C
- **Key Concepts:** Token recognition (Keywords, Identifiers, Operators, Delimiters)

### 3. Valid Arithmetic Expression Parser
- **Tools / Languages:** LEX & YACC
- **Key Concepts:** Context-free grammar, precedence, and syntax parsing

### 4. Valid Variable Recognition
- **Tools / Languages:** LEX & YACC
- **Key Concepts:** Grammar rules for valid identifier naming conventions

### 5. Recognition of C Control Structures
- **Tools / Languages:** LEX & YACC
- **Key Concepts:** Syntax analysis of if-else, while, for, and switch

### 6. Calculator Implementation
- **Tools / Languages:** LEX & YACC
- **Key Concepts:** Arithmetic expression evaluation with precedence rules

### 7. Three-Address Code (TAC) Generation
- **Tools / Languages:** LEX & YACC
- **Key Concepts:** Intermediate Code Generation (ICG) with temporary variables

### 8. Type Checking
- **Tools / Languages:** C
- **Key Concepts:** Semantic analysis and type mismatch detection

### 9. Code Optimization Techniques
- **Tools / Languages:** C
- **Key Concepts:** Machine-independent optimization (Constant Folding, Strength Reduction)

### 10. Compiler Back-End (8086 Code Gen)
- **Tools / Languages:** C
- **Key Concepts:** Code generation converting TAC to 8086 assembly instructions

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/sri-kumaran-ct/CompilerDesign_experiments.git
cd CompilerDesign_experiments
```

### 2. Navigate to an Experiment

Each experiment folder contains its own self-contained `README.md` file with the required prerequisites, algorithms, source code, compilation steps, sample inputs, and expected outputs.

For example:

```bash
cd experiment7
cat README.md
```

### 3. Compile and Run

For **C-based experiments**:

```bash
gcc main.c -o output
./output
```

For **LEX & YACC-based experiments**:

```bash
lex filename.l
yacc -d filename.y
gcc lex.yy.c y.tab.c -o output
./output
```

> **Note:** The exact filenames and compilation commands may vary depending on the experiment. Always refer to the individual experiment's `README.md` for the specific instructions.

---

## Prerequisites & Compilation Tools

To run all experiments, make sure you have the following installed on your machine:

* **GCC Compiler** (`gcc`)
* **Flex / Lex** (`lex` or `flex`)
* **Bison / Yacc** (`yacc` or `bison`)

### Installation Commands

#### Ubuntu / Debian

```bash
sudo apt update
sudo apt install build-essential flex bison
```

#### macOS (via Homebrew)

```bash
brew install gcc flex bison
```

---

## General Compilation Steps

### For C Programs

**Experiments:** 1, 2, 8, 9, 10

```bash
gcc main.c -o output
./output
```

### For LEX & YACC Programs

**Experiments:** 3, 4, 5, 6, 7

```bash
lex filename.l
yacc -d filename.y
gcc lex.yy.c y.tab.c -o output
./output
```

> **Note:** Depending on your system and the specific experiment, you may need to link the Lex library using `-ll` or use `flex`/`bison` instead of `lex`/`yacc`.

---

## Detailed Documentation

Each individual experiment directory contains its own dedicated `README.md` with:

* **Aim**
* **Detailed Step-by-Step Algorithm**
* **Specific Compilation Steps**
* **Sample Inputs and Expected Outputs**
