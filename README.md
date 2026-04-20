# CFG to GNF Converter — Theory of Computation

> A step-by-step implementation for converting a **Context-Free Grammar (CFG)** into **Greibach Normal Form (GNF)** as part of the Theory of Computation course.
where `a` is a **terminal** and `α` is a (possibly empty) string of **variables**.

GNF is useful in proving theoretical results about context-free languages and is used in constructing top-down parsers without left recursion.

---

## 📚 What is GNF?

A CFG is in **Greibach Normal Form** if every production rule satisfies:
- The right-hand side starts with exactly **one terminal symbol**
- Followed by **zero or more non-terminals**

**Example:**

| Before (CFG) | After (GNF) |
|---|---|
| `S → AB` | `S → aB` |
| `A → a` | Terminals lead every rule |

---

## ⚙️ Conversion Steps

The conversion from CFG to GNF follows these major steps:

1. **Eliminate ε-productions** (Nullable variables)
2. **Eliminate Unit Productions** (A → B)
3. **Eliminate Useless Symbols** (unreachable/non-generating)
4. **Convert to Chomsky Normal Form (CNF)** *(intermediate step)*
5. **Order the non-terminals** (A₁, A₂, ..., Aₙ)
6. **Eliminate left recursion** using substitution
7. **Apply Lemma substitutions** to ensure all rules start with a terminal

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/your-username/cfg-to-gnf.git
cd cfg-to-gnf

# Run the program
python main.py
```

> Replace `python main.py` with the appropriate command for your language (Java, C++, etc.)

---

## 📥 Input Format

Provide the grammar as production rules. Example:
---

## 📌 About

This project implements the algorithm to convert any Context-Free Grammar (CFG) into **Greibach Normal Form (GNF)**, where every production rule is of the form:
