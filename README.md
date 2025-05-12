# LL(1) and SLR(1) Grammar Analyzer

## Group Members
- Alyson Henao  
- Nathalia Cardoza  
- Samuel Arango  

## Environment and Tools
- **Operating System:** Windows 11 / Ubuntu 22.04 LTS (tested on both)  
- **Programming Language:** Python 3.10  
- **Tools/Libraries Used:** No external libraries required; standard Python only.  

## Description
This project implements a class called `Grammar` that allows you to:

- Define a context-free grammar using a dictionary format.
- Automatically compute **FIRST** and **FOLLOW** sets.
- Check whether the grammar is **LL(1)** or **SLR(1)**.
- Parse input strings using an LL(1) parsing algorithm.

## How to Run

1. **Clone or Download the Repository**
   ```bash
   git clone https://github.com/your-repo/grammar-analyzer.git
   cd grammar-analyzer
Create a Python File (e.g., main.py)
Copy the Grammar class implementation into this file or import it if it’s in a separate module.

Example Usage:

python
Copiar
Editar
from grammar import Grammar  # If you saved the class in grammar.py

productions = {
    'S': [['a', 'A', 'b'], ['e']],
    'A': [['c'], ['S']]
}

g = Grammar(productions)

print("FIRST sets:")
for nt, s in g.first_sets.items():
    print(f"{nt}: {s}")

print("\nFOLLOW sets:")
for nt, s in g.follow_sets.items():
    print(f"{nt}: {s}")

print("\nIs LL(1)?", g.check_ll1())
print("Is SLR(1)?", g.check_slr1())
print("Parse input 'acb':", g.parse_ll1("acb"))
Run the Script:

bash
Copiar
Editar
python main.py
Notes
Input strings should not include spaces between characters.

The end-of-input marker ($) is automatically added by the parser.

The grammar must use 'e' to represent epsilon (empty string).
