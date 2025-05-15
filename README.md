
# LL(1) and SLR(1) Parser Implementation

## 👩🏻‍💻👩🏼‍💻👨🏽‍💻 Group Members 👩🏻‍💻👩🏼‍💻👨🏽‍💻
- Alyson Henao
- Nathalia Cardoza
- Samuel Arango

## ✅ System Requirements ✅
- **Operating System**: Windows 10/11, macOS 10.15+, or Linux (Ubuntu 20.04+ recommended)
- **Python Version**: 3.8 or higher
- **Dependencies**: None (uses only standard Python libraries)

## 📖 Project Description 📖
This implementation provides both LL(1) and SLR(1) parsers for context-free grammars. The program can:
1. Determine whether a grammar is LL(1), SLR(1), both, or neither
2. Parse input strings using the appropriate parser
3. Compute FIRST and FOLLOW sets for grammar analysis

## 📲 Installation 📲
No installation is required beyond having Python 3.8+ installed. To check your Python version:
```bash
python --version
```

## 🗺 Usage Instructions 🗺

### ⚡Running the Program ⚡
1. Save the code to a file named `main.py`
2. Run the program from command line:
```bash
python main.py
```

### 👾 Input Format 👾
The program expects input in the following format:

1. First line: Number of grammar productions (N)
2. Next N lines: Grammar productions in the format:
   ```
   NonTerminal -> production1 | production2 | ...
   ```
   Where productions are separated by spaces (use 'e' for ε/epsilon)

3. After the grammar, enter strings to parse (one per line)
4. Enter a blank line to finish input

### 👀 Example Session 👀
```
3
S -> A B
A -> a e
B -> b C
C -> c
aabbcc
ab
(blank line)
```

### 📌 Parser Selection 📌
If the grammar is both LL(1) and SLR(1), you'll be prompted to choose:
- `T` for LL(1) parser
- `B` for SLR(1) parser
- `Q` to quit

## 🗂 Features 🗂
- Automatic grammar classification (LL1/SLR1/both/neither)
- Interactive parser selection when applicable
- Detailed FIRST and FOLLOW set computation
- Comprehensive error handling

## 📝 Implementation Notes 📝
- The program uses '$' as end-of-input marker
- Epsilon/empty productions are represented by 'e'
- Non-terminals must be uppercase letters
- Terminals must be lowercase letters or symbols

## 🪄 Output Interpretation 🪄
- "yes": Input string is accepted by the grammar
- "no": Input string is rejected by the grammar
- Error messages will indicate if the grammar is not LL(1) or SLR(1)

## ❌ Limitations ❌
- Grammar must have a start symbol 'S'
- Left recursion makes a grammar non-LL(1)
- Certain ambiguous grammars may be rejected even if they're technically SLR(1)

## 💡Troubleshooting 💡
If you encounter issues:
1. Verify your Python version meets requirements
2. Check that input follows the specified format
3. Ensure non-terminals are uppercase and terminals are lowercase
4. Make sure productions are separated by spaces
