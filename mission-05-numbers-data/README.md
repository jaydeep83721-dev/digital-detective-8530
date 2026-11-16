# Mission 5 — Numbers and Data

## 1. Task / Objective

The objective of this mission is to understand how computers represent numbers and text using binary data.

The activities involve converting numbers between decimal, binary, and hexadecimal, verifying the results using Python, creating a number-conversion program, and exploring character encoding.

## 2. Work Completed

### Task 5.1 — Convert Numbers by Hand

I performed seven number-system conversions using division, positional values, and hexadecimal digit representations.

**1. Decimal 13 to Binary**

Repeated division by 2:

| Division | Quotient | Remainder |
|---|---|---|
| 13 ÷ 2 | 6 | 1 |
| 6 ÷ 2 | 3 | 0 |
| 3 ÷ 2 | 1 | 1 |
| 1 ÷ 2 | 0 | 1 |

Reading remainders from bottom to top:

**(13)₁₀ = (1101)₂**

**2. Decimal 25 to Binary**

| Division | Quotient | Remainder |
|---|---|---|
| 25 ÷ 2 | 12 | 1 |
| 12 ÷ 2 | 6 | 0 |
| 6 ÷ 2 | 3 | 0 |
| 3 ÷ 2 | 1 | 1 |
| 1 ÷ 2 | 0 | 1 |

**(25)₁₀ = (11001)₂**

**3. Binary 1010 to Decimal**

1010 = 1×2³ + 0×2² + 1×2¹ + 0×2⁰

= 8 + 0 + 2 + 0 = **10**

**4. Binary 1101 to Decimal**

1101 = 1×2³ + 1×2² + 0×2¹ + 1×2⁰

= 8 + 4 + 0 + 1 = **13**

**5. Hexadecimal A to Decimal**

A represents decimal 10.

**(A)₁₆ = (10)₁₀**

**6. Hexadecimal 1F to Decimal**

1F = 1×16¹ + 15×16⁰

= 16 + 15 = **31**

**7. Binary 1111 to Hexadecimal**

1111 = 8 + 4 + 2 + 1 = 15

Decimal 15 is represented by F in hexadecimal.

**(1111)₂ = (F)₁₆**

### Task 5.2 — Verify Conversions Using Python

I used the Python interactive environment to verify my manual calculations.

| Python Expression | Output | Matches Manual Result? |
|---|---|---|
| `bin(13)` | `0b1101` | Yes |
| `bin(25)` | `0b11001` | Yes |
| `int("1010", 2)` | `10` | Yes |
| `int("1101", 2)` | `13` | Yes |
| `int("A", 16)` | `10` | Yes |
| `int("1F", 16)` | `31` | Yes |
| `hex(int("1111", 2))` | `0xf` | Yes |
| `hex(31)` | `0x1f` | Yes |
| `hex(15)` | `0xf` | Yes |

All results matched the manual calculations.

### Task 5.3 — Build a Small Number Converter

I created a Python program named `number_converter.py` that accepts a decimal integer and displays its binary and hexadecimal representations.

Program:

```python
number = int(input("Enter a decimal number: "))

binary = bin(number)
hexadecimal = hex(number)

print("Binary:", binary)
print("Hexadecimal:", hexadecimal)
```

Command used to execute the program:

```bash
python3 number_converter.py
```

**Test Cases**

| Test Number | Binary Output | Hexadecimal Output |
|---|---|---|
| 13 | `0b1101` | `0xd` |
| 25 | `0b11001` | `0x19` |
| 31 | `0b11111` | `0x1f` |

The program was tested using three different positive decimal numbers.

**How the Program Works**

1. `input()` receives the number entered by the user as text.
2. `int()` converts the entered text into an integer.
3. `bin()` produces the binary representation.
4. `hex()` produces the hexadecimal representation.
5. `print()` displays the converted values.

The prefixes `0b` and `0x` identify binary and hexadecimal values, respectively.

### Task 5.4 — How Is Text Stored?

Computers use character-encoding standards to represent text as numbers and bytes.

ASCII supports a basic set of characters, while UTF-8 can represent a much wider variety of characters.

**ASCII Character Codes**

| Character | Decimal ASCII Code | 8-bit Binary |
|---|---|---|
| A | 65 | 01000001 |
| a | 97 | 01100001 |

I verified these values using Python:

```python
ord("A")
ord("a")
bin(ord("A"))
bin(ord("a"))
```

The results matched the expected values.

**Why Are Encoding Standards Necessary?**

Encoding standards provide a consistent way to represent characters using bytes. This allows computers to store, exchange, and display text correctly.

**Example of a Non-ASCII Character**

The Indian Rupee symbol (₹) is not included in basic ASCII.

I tested its UTF-8 representation using:

```python
"₹".encode("utf-8")
```

Observed output:

```text
b'\xe2\x82\xb9'
```

This shows that the rupee symbol is represented using three bytes in UTF-8.

## 3. Commands / Tools Used

| Command / Function | Purpose |
|---|---|
| `python3` | Start the Python interpreter. |
| `python3 number_converter.py` | Execute the converter program. |
| `input()` | Accept user input. |
| `int()` | Convert text into an integer or interpret digits in a specified base. |
| `bin()` | Produce a binary representation. |
| `hex()` | Produce a hexadecimal representation. |
| `ord()` | Obtain the Unicode code point of a character. |
| `.encode("utf-8")` | Encode text into UTF-8 bytes. |
| `print()` | Display output. |
| Visual Studio Code | Write and edit the Python program. |

## 4. My Understanding

Through these activities, I learned that computers use binary digits to represent information.

Decimal, binary, and hexadecimal are different number systems used to express numerical values.

Python provides built-in functions that simplify conversion between these representations.

I also learned that text must be encoded before being stored as bytes. ASCII supports basic characters, while UTF-8 can represent characters from many languages and symbols.

## 5. Difficulties Faced

During the Python interactive activity, I initially entered multiple expressions while the interpreter was showing the continuation prompt (`...`), so the commands did not execute as expected.

## 6. How I Resolved Them

I interrupted the incomplete input using `Control + C`, returned to the normal Python prompt (`>>>`), and executed each expression separately.

After that, the conversions produced the expected results.

## 7. Evidence / Files

The Mission 5 folder contains:

```text
mission-05-numbers-data/
├── README.md
└── number_converter.py
```

- `README.md` — Manual conversions, Python verification, converter test cases, character encoding, and learning outcomes.
- `number_converter.py` — Working decimal-to-binary and decimal-to-hexadecimal converter.

## 8. Commit Details

**Planned commit message:** `Build number converter and practise data representation`

**Repository:** https://github.com/jaydeep83721-dev/digital-detective-8530

**Push verification:** To be completed after committing and pushing Mission 5.
