# Mission 4 — How Programs Run

## 1. Task / Objective

The objective of Mission 4 is to understand how programs are executed and compare the roles of compilers and interpreters.

The mission involves creating a simple Python program, running it through Terminal, and understanding how source code is translated or executed.

## 2. Work Completed

### Task 4.1 — Create and Run a Python Program

I created a Python file named `hello.py` inside the `mission-04-programs` directory using Visual Studio Code.

The program contains:

```python
print("Hello from Python")
```

I saved the file and ran it from Terminal using:

```bash
python3 hello.py
```

**Expected output:**

```text
Hello from Python
```

When the program ran successfully, Python executed the `print()` instruction and displayed the message in Terminal.

### Task 4.2 — Compare Compiler and Interpreter

| Point | Compiler | Interpreter |
|---|---|---|
| When translation / execution happens | Translates source code into another form before the compiled program runs. | Executes program instructions at runtime. |
| Typical output | Compiled code, often an executable. | Results produced while executing instructions. |
| One example | GCC for C programs. | Python interpreter. |
| One advantage | Native compiled programs can execute efficiently. | Programs can be tested and executed without a separate manual compilation step. |

### Explanation

A compiler translates source code into another form before the resulting program is executed. An interpreter executes program instructions at runtime. Compiled native programs can offer efficient execution, whereas interpreters make it convenient to run and test programs. Some implementations, such as Python, combine compilation into bytecode with execution by a virtual machine.

## 3. Commands / Tools Used

| Command / Tool | Purpose |
|---|---|
| Visual Studio Code | Created and edited the Python program. |
| `touch hello.py` | Created an empty Python file. |
| `python3 hello.py` | Executed the program using Python 3. |
| `print()` | Displayed a message in Terminal. |
| macOS Terminal | Ran the Python program and displayed its output. |

## 4. My Understanding

I learned that a program contains instructions written in a programming language.

When I executed `hello.py`, Python processed the instructions and displayed the output in Terminal.

I also understood that compilers and interpreters use different approaches to translating or executing programs. Real language implementations may combine these approaches.

## 5. Difficulties Faced

No major difficulties were encountered while creating and executing the Python program.

## 6. How I Resolved Them

Not applicable.

## 7. Evidence / Files

The Mission 4 directory contains:

```text
mission-04-programs/
├── README.md
└── hello.py
```

- `hello.py` — The working Python program.
- `README.md` — The mission documentation, comparison table, explanations, and learning outcomes.

## 8. Commit Details

**Commit message:** `Compare compilers and interpreters`

**Repository:** https://github.com/jaydeep83721-dev/digital-detective-8530

**Commit:** `74a8801` — Compare compilers and interpreters.

**Push status:** Successfully pushed to GitHub.
