# PDA and CFG – Case Studies

## 📌 Project Overview

This project demonstrates the practical implementation of **Pushdown Automata (PDA)** and **Context-Free Grammars (CFG)** using Python.

Unlike Finite Automata, Pushdown Automata use an additional stack to process context-free languages that require memory for matching and nested structures.

This project implements three case studies:
1. Balanced Parentheses Validation
2. Arithmetic Expression Syntax Validation
3. Centre-Marked Palindrome Checking

## 🎯 Objectives

- Understand the working principles of Pushdown Automata.
- Explore the importance of stack operations in automata.
- Implement PDA-based language recognition using Python.
- Understand Context-Free Grammars and their applications.
- Validate arithmetic expressions using CFG.
- Test accepted and rejected input strings.

## 🛠️ Technologies Used

- Python
- Google Colab
- Pandas
- Matplotlib

## 🔍 Case Studies Implemented

### 1. Balanced Parentheses

This case study uses a Pushdown Automaton to check whether parentheses are properly balanced.

**Working Principle:**
- `Z0` is used as the initial stack symbol.
- For every opening parenthesis `(`, the PDA pushes `X` onto the stack.
- For every closing parenthesis `)`, the PDA pops `X` from the stack.
- If the input ends and only `Z0` remains, the string is accepted.
- Unmatched parentheses are rejected.

**Accepted Examples:**
- `()`
- `(())`
- `()()`
- `((()()))`

### 2. Arithmetic Syntax Validation using CFG

This case study uses a Context-Free Grammar to validate arithmetic expressions.

**Grammar Used:**

```text
E → E + T | T
T → T * F | F
F → (E) | id
```

**Working Principle:**
- `E` represents expressions.
- `T` represents terms.
- `F` represents factors.
- Addition and multiplication are handled at different grammar levels.
- Parentheses are used for grouping expressions.
- A stack-based parser checks whether an expression follows the grammar.

**Accepted Examples:**
- `id`
- `id+id`
- `id*id+id`
- `(id+id)*id`
- `id*(id+id*id)`

### 3. Centre-Marked Palindrome Checking

This case study implements a PDA for the language:

`w c w^R`

Here, `c` is the centre marker and `w^R` represents the reverse of the first part.

**Working Principle:**
- The PDA pushes `A` for every `a`.
- It pushes `B` for every `b`.
- When it reads the centre marker `c`, it switches to the matching phase.
- It pops `A` when reading `a` and `B` when reading `b`.
- If the input ends and only `Z0` remains, the string is accepted.

**Accepted Examples:**
- `c`
- `aca`
- `bcb`
- `abbcbba`
- `baacaab`

## ⚙️ Stack Operations

The project demonstrates the following stack operations:

| Operation | Description |
|---|---|
| Push | Adds a symbol to the stack |
| Pop | Removes the top symbol |
| Peek | Checks the top stack symbol |
| Accept | Confirms the input follows the required language |

## 🧪 Testing and Results

The project includes 30 test strings across all three case studies.

| Case Study | Test Cases |
|---|---:|
| Balanced Parentheses | 10 |
| Arithmetic CFG | 10 |
| Palindrome PDA | 10 |
| **Total** | **30** |

**Expected Verification Result:**
- Total Tests: 30
- Passed: 30
- Failed: 0
- Verification Status: ALL TESTS PASSED (100%)

## 🚀 How to Run the Project

1. Download or clone this repository.
2. Open the `.ipynb` notebook using Google Colab.
3. Select **Runtime → Run all**.
4. Observe the PDA execution traces, parsing results, stack operations, and final verification summary.

No external dataset is required.

## 📂 Project Structure

```text
PDA-CFG-Case-Studies/
│
├── Task_3_PDA_CFG_Case_Studies.ipynb
└── README.md
```

## 📚 Learning Outcomes

- Understanding Pushdown Automata.
- Understanding Context-Free Grammars.
- Learning stack-based language recognition.
- Implementing push and pop operations.
- Understanding arithmetic expression parsing.
- Recognizing balanced parentheses and palindromes.
- Comparing Finite Automata with Pushdown Automata.

## ⚠️ Limitations

- The balanced-parentheses PDA supports parentheses only.
- The arithmetic parser supports identifiers (`id`), addition, multiplication, and parentheses.
- The palindrome PDA requires a centre marker `c` and uses `a` and `b` as input symbols.
- The implementations demonstrate language recognition and do not represent complete programming-language compilers.

## 👨‍💻 Academic Information

**Course:** 21CSC301T – Formal Language and Automata

**Assessment:** CLA-2 – Task 3

**Institution:** SRM Institute of Science and Technology, Tiruchirappalli

---

*Developed as part of the Formal Language and Automata coursework.*
