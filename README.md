Claro, aquí tienes el contenido listo para copiar y pegar en tu archivo `README.md`:

````markdown
# Grammar Analyzer: LL(1) and SLR(1) Parser

## 👥 Authors
- Alyson Henao  
- Nathalia Cardoza  
- Samuel Arango  

## 🖥️ Environment and Tools Used
- **Operating System**: Windows 11 and Ubuntu 22.04  
- **Programming Language**: Python 3.10+  
- **Editor**: Visual Studio Code / PyCharm / Terminal + Vim  
- **Version Control**: Git  

## 📋 Project Description
This project implements a grammar analyzer for formal languages, supporting:
- Computation of **FIRST** and **FOLLOW** sets
- Verification of **LL(1)** grammar compliance
- **LL(1) Parsing** of input strings
- Preliminary implementation and verification of **SLR(1)** grammar compliance

The tool is designed to aid in compiler design, language parsing, and automata theory education.

## ▶️ How to Run the Project

### 1. Requirements
Make sure you have Python installed. You can check by running:
```bash
python --version
````

If Python is not installed, download and install it from: [https://www.python.org/downloads/](https://www.python.org/downloads/)

### 2. Clone or Download the Repository

```bash
git clone https://github.com/your-repo/grammar-analyzer.git
cd grammar-analyzer
```

Or simply download the `.py` file and place it in your working directory.

### 3. Run the Python Script

Create a Python script (e.g., `main.py`) with the following example usage:

```python
from grammar import Grammar  # Replace with the actual filename if needed

productions = {
    'S': [['a', 'A'], ['b']],
    'A': [['c'], ['e']]  # 'e' represents epsilon
}

grammar = Grammar(productions)

print("FIRST sets:")
for nt in grammar.first_sets:
    print(f"FIRST({nt}) = {grammar.first_sets[nt]}")

print("\nFOLLOW sets:")
for nt in grammar.follow_sets:
    print(f"FOLLOW({nt}) = {grammar.follow_sets[nt]}")

print("\nLL(1) check:", grammar.check_ll1())

input_string = "ac$"  # Make sure the string ends with '$'
print("\nParsing result:", grammar.parse_ll1(input_string))
```

Then run the script:

```bash
python main.py
```

### 4. Expected Output Example

```
FIRST sets:
FIRST(S) = {'a', 'b'}
FIRST(A) = {'c', 'e'}
...

FOLLOW sets:
FOLLOW(S) = {'$'}
FOLLOW(A) = {'$'}

LL(1) check: True

Parsing result: True
```

## 📌 Notes

* The grammar must be provided as a dictionary where keys are nonterminals and values are lists of production alternatives.
* Use `'e'` to denote ε (epsilon).
* All strings to parse should end with the dollar sign (`$`) to represent the end of input.


