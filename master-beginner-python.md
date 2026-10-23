# Python Programming: Master Beginner Guide & Curriculum

> **A Complete, Rich, and Pedagogically Balanced Foundation in Python**
> *Designed for absolute beginners to intermediate progression with practical code examples, conceptual clarity, advanced textual references, and hands-on Code Skeleton Exams.*

---

## Table of Contents

1- [Getting Started: Introduction & Environment](#1-getting-started-introduction--environment)
2- [Core Syntax, Variables & Memory Model](#2-core-syntax-variables--memory-model)
3- [Standard Input, Output & Type Casting](#3-standard-input-output--type-casting)
4- [Fundamental Data Types & Operators](#4-fundamental-data-types--operators)
5- [Working with Strings & Text Manipulation](#5-working-with-strings--text-manipulation)
6- [Control Flow: Conditional Decision Making](#6-control-flow-conditional-decision-making)
7- [Control Flow: Loops & Iteration](#7-control-flow-loops--iteration)
8- [Data Collections: Lists, Tuples, Sets & Dictionaries](#8-data-collections-lists-tuples-sets--dictionaries)
9- [Functions, Modular Design & Scope](#9-functions-modular-design--scope)
10- [Error Handling & Exception Safety](#10-error-handling--exception-safety)
11- [File I/O & Structured Data Handling](#11-file-io--structured-data-handling)
12- [Modules, Standard Library & Virtual Environments](#12-modules-standard-library--virtual-environments)
13- [Introduction to Object-Oriented Programming (OOP)](#13-introduction-to-object-oriented-programming-oop)
14- [Comprehensive Capstone Practice Projects](#14-comprehensive-capstone-practice-projects)
15- [Python Best Practices & Specialization Learning Roadmap](#15-python-best-practices--specialization-learning-roadmap)



---

## 1. Getting Started: Introduction & Environment

### 1.1 What is Python?

Python is an open-source, high-level, interpreted, general-purpose programming language created by **Guido van Rossum** and first released in 1991. Python is renowned for its clean syntax, code readability, and vast ecosystem of standard and third-party libraries.

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│                          Core Architectural Traits                          │
├───────────────────┬─────────────────────────────────────────────────────────┤
│ High-Level        │ Abstracts away low-level memory allocation and hardware │
│                   │ registers, allowing developers to focus on logic.       │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ Interpreted       │ Source instructions are executed sequentially without   │
│                   │ requiring manual compilation into machine binaries.     │ 
├───────────────────┼─────────────────────────────────────────────────────────┤
│ Dynamically Typed │ Types are bound to values at runtime rather than        │
│                   │ explicitly declared in code before execution.           │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ Multi-Paradigm    │ Naturally supports Procedural, Object-Oriented, and     │
│                   │ Functional programming methodologies.                   │
└───────────────────┴─────────────────────────────────────────────────────────┘
```

### 1.2 Why Python? Ecosystem & Career Domains

Python powers major platforms, enterprise systems, scientific computing, and startup infrastructure globally:

* **Data Science, Machine Learning & AI:** TensorFlow, PyTorch, Pandas, Scikit-Learn.
* **Web Development & APIs:** FastAPI, Django, Flask.
* **Scripting & Automation:** Web scraping, data pipeline scheduling, desktop automation.
* **DevOps & Cloud Infrastructure:** AWS CDK, Ansible, Docker automation scripts.
* **Cybersecurity & Networking:** Packet crafting, vulnerability scanning tools.

### 1.3 How Python Works (Beginner Mental Model)

When you write Python code, you save plain text files ending with `.py`. When you instruct Python to run your file, the Python interpreter reads your code line by line and translates it into operations executed directly by your computer.

```text
[ Python Source File (.py) ]
              │
              ▼
    [ Python Interpreter ] ───► Executes code sequentially line by line
              │
              ▼
    [ Console Output / Action ]
```

> [!NOTE]
> **Advanced Text Reference: Bytecode, AST & The Python Virtual Machine (PVM)**
> Behind the scenes, CPython (the standard reference implementation) first parses source text into an **Abstract Syntax Tree (AST)**, compiles it into optimized intermediate **bytecode** (`.pyc` files stored in `__pycache__`), and evaluates this bytecode inside the **Python Virtual Machine (PVM)** against host CPU and memory resources.

### 1.4 Setting Up the Environment

1. **Download:** Navigate to [python.org/downloads](https://www.python.org/downloads/) and download the latest stable release (Python 3.12+).
2. **Install (Windows Important Step):** During installation, check the box labeled **"Add python.exe to PATH"**.
3. **Verification:** Open your terminal (PowerShell, Command Prompt, or macOS/Linux Terminal) and verify:
   ```bash
   python --version
   pip --version
   ```
4. **Editor:** Use a modern code editor such as **Visual Studio Code (VS Code)** with the official Microsoft Python extension installed.

### 1.5 Interactive REPL vs. Script Execution

* **Interactive REPL (Read-Eval-Print Loop):** Type `python` in your terminal without arguments. A prompt (`>>>`) opens where you can test single lines of code immediately. Exit by typing `exit()`.
* **Script Execution (`.py`):** Author your logic in a saved file and run:
  ```bash
  
  python my_script.py
  ```

### 1.6 Writing and Running Your First Script

Create a file named `hello.py` and write:

```python
# hello.py - My first Python script
print("System initialized.")
print("Welcome to Python programming!")

```

Run the script in your terminal:
```bash
python hello.py
```

*Output:*
```text
System initialized.
Welcome to Python programming!
```

---

### 1.7 Module 1 Code Skeleton Exam

**Objective:** Complete the script skeleton to output system configuration details.

```python
# ==========================================
# MODULE 1 EXAM: SYSTEM BANNER SKELETON
# ==========================================

# TODO 1: Print a top border made of 30 equal signs '='
print(________)

# TODO 2: Print the application title: "PYTHON ENVIRONMENT VERIFIED"
print(________)

# TODO 3: Print a bottom border made of 30 equal signs '='
print(________)
```

<details>
<summary><b>View Solution</b></summary>

```python
print("=" * 30)
print("PYTHON ENVIRONMENT VERIFIED")
print("=" * 30)
```
</details>

---

## 2. Core Syntax, Variables & Memory Model

### 2.1 What is a Variable?

A **variable** is a named reference (label) that points to a value stored in your computer's memory. In Python, variables are dynamically created upon assignment using the `=` assignment operator:

```python
app_name = "CloudSync"  # String assigned to app_name
port_number = 8080      # Integer assigned to port_number
is_active = True        # Boolean assigned to is_active
```

```text
Variable Name (Label)          Value in Memory
┌──────────────────┐           ┌────────────────────┐
│   app_name       ├──────────►│ "CloudSync" (str)  │
├──────────────────┤           ├────────────────────┤
│   port_number    ├──────────►│ 8080 (int)         │
└──────────────────┘           └────────────────────┘
```

### 2.2 Identifier Naming Rules and PEP 8 Conventions 

To write valid and clean Python code:

```text
9_age
┌───────────────────────────────────────┬───────────────────────────────────────┐
│         Syntax Rules (Enforced)       │       PEP 8 Conventions (Best Style)  │
├───────────────────────────────────────┼───────────────────────────────────────┤
│ • Must begin with a letter or `_`     │ • Use snake_case for variables &      │
│ • Cannot start with a number (0-9)    │   functions (e.g., `user_account`)    │
│ • Only contain letters, numbers, `_`  │ • Use UPPER_CASE for fixed constants  │
│ • Case-sensitive (`total` != `Total`) │   (e.g., `MAX_RETRIES = 3`)           │
│ • Cannot use reserved Python keywords │ • Use descriptive, meaningful names   │ 
└───────────────────────────────────────┴───────────────────────────────────────┘
```

### 2.3 Comments and Documentation

```python
# 1. Single-line comment explaining why a step is taken
timeout_seconds = 30  # Inline comment

"""
2. Multi-line comment (or Docstring)
Used for comprehensive explanations, module headers,
or documenting functions and classes.
"""
```

### 2.4 Reserved Keywords

Python reserves 35 special words that cannot be used as variable names:
`False`, `None`, `True`, `and`, `as`, `assert`, `break`, `class`, `continue`, `def`, `del`, `elif`, `else`, `except`, `finally`, `for`, `from`, `global`, `if`, `import`, `in`, `is`, `lambda`, `nonlocal`, `not`, `or`, `pass`, `raise`, `return`, `try`, `while`, `with`, `yield`, `match`, `case`.

### 2.5 Indentation and Code Blocks

Instead of curly braces `{}` or `BEGIN/END` markers, Python uses **whitespace indentation** (4 spaces) to define code blocks and structural hierarchy:

```python
# Clean 4-space indentation defines block scope
status_code = 200

if status_code == 200:
    print("Connection established successfully.")
    print("Beginning telemetry download.")
print("This line runs unconditionally outside the if-block.")
```

---

### 2.6 Module 2 Code Skeleton Exam

**Objective:** Complete the user profile card skeleton with proper variable assignments following PEP 8 naming conventions.

```python
# ==========================================
# MODULE 2 EXAM: PROFILE CARD SKELETON
# ==========================================

# TODO 1: Define a constant MAX_LOGIN_ATTEMPTS set to 5
MAX_LOGIN_ATTEMPTS = ________

# TODO 2: Assign appropriate variable values in snake_case
first_name = "jordan"________       # Assign "Jordan"
account_id = 10452 ________       # Assign integer 10452
account_balance = 56789.98 ________  # Assign float 1250.75
is_verified = ____True____      # Assign boolean True

# TODO 3: Print each variable along with its type using type()
print("Name:", first_name, "| Type:", type(first_name))
print("Account ID:", account_id, "| Type:", type(account_id))
print("Balance: $", account_balance, "| Type:", type(account_balance))
print("Verified:", is_verified, "| Type:", type(is_verified))
print("Max Attempts Allowed:", MAX_LOGIN_ATTEMPTS)
```

<details>
<summary><b>View Solution</b></summary>

```python
MAX_LOGIN_ATTEMPTS = 5

first_name = "Jordan"
account_id = 10452
account_balance = 1250.75
is_verified = True

print("Name:", first_name, "| Type:", type(first_name))
print("Account ID:", account_id, "| Type:", type(account_id))
print("Balance: $", account_balance, "| Type:", type(account_balance))
print("Verified:", is_verified, "| Type:", type(is_verified))
print("Max Attempts Allowed:", MAX_LOGIN_ATTEMPTS)
```
</details>
---

## 3. Standard Input, Output & Type Casting

### 3.1 Console Output with `print()`

The built-in `print()` function sends text representations to the standard console stream:

```python
# Signature: print(*objects, sep=' ', end='\n')

# 1. Custom separator (sep)
print("2026", "10", "02", sep="-")  # Output: 2026-10-02

# 2. Custom line ending (end)
print("Processing data", end="...")
print("Done!")  # Output: Processing data...Done! (on the exact same line)
```

### 3.2 User Input with `input()`

The `input()` function pauses program execution, displays an optional prompt to the user, waits for keyboard input followed by `Enter`, and returns what was typed.

```python
user_city = input("Enter your current city: ")
print("Logged location:", user_city)
```

### 3.3 String Return Nature and Explicit Type Conversion

> [!WARNING]
> **The Input String Trap:** The `input()` function **always** returns a string (`str`). Adding two raw inputs concatenates text rather than calculating a mathematical sum.

```python
# ❌ BUG: Concatenation instead of arithmetic addition
val1 = input("Enter number 1: ")  # User types 10 -> "10"
val2 = input("Enter number 2: ")  # User types 20 -> "20"
print(val1 + val2)                # Outputs: "1020"

# ✅ CORRECT: Explicit type conversion
num1 = float(input("Enter number 1: "))  # 10.0
num2 = float(input("Enter number 2: "))  # 20.0
print("Arithmetic Sum:", num1 + num2)   # 30.0
```

#### Built-in Type Constructors
* `int(x)`: Converts to integer whole number (`int("42")` $\rightarrow 42$).
* `float(x)`: Converts to decimal number (`float("3.14")` $\rightarrow 3.14$).
* `str(x)`: Converts object to string text representation (`str(100)` $\rightarrow$ `"100"`).
* `bool(x)`: Converts value to truth boolean (`bool(0)` $\rightarrow `False`, `bool(1)` $\rightarrow `True`).

### 3.4 Practical CLI Prompt Design

```python
# Clean interactive prompt pattern
print("\n--- CURRENCY CONVERTER CLI ---")
usd_amount = float(input("Enter amount in USD ($): "))
exchange_rate = float(input("Enter conversion rate to EUR: "))
eur_total = usd_amount * exchange_rate
print(f"${usd_amount:.2f} USD is equivalent to €{eur_total:.2f} EUR")
```

---

---

## 4. Fundamental Data Types & Operators

### 4.1 Primitive Numeric Types (`int`, `float`, `complex`)

```python
whole_count = 100         # int: arbitrary precision whole numbers
price = 19.95             # float: IEEE 754 floating-point decimals
complex_val = 3 + 4j      # complex: real and imaginary parts
```

### 4.2 Boolean Logic (`bool`) and `NoneType`

* **`bool`:** Subclass of integers containing only `True` (equivalent to `1`) or `False` (equivalent to `0`).
* **`NoneType`:** Contains the singleton object `None`, representing the intentional absence of a value.

### 4.3 Arithmetic and Augmented Assignment Operators

| Operator | Operation | Example (`a = 15, b = 4`) | Result |
| :---: | :--- | :---: | :---: |
| `+` | Addition | `a + b` | `19` |
| `-` | Subtraction | `a - b` | `11` |
| `*` | Multiplication | `a * b` | `60` |
| `/` | True Division (Always returns `float`) | `a / b` | `3.75` |
| `//` | Floor Division (Rounds down to integer) | `a // b` | `3` |
| `%` | Modulus (Remainder of division) | `a % b` | `3` | 
| `**` | Exponentiation (Power) | `2 ** 3` | `8` |


#### Augmented Assignment Short-Hands
`x += 5` ($x = x + 5$), `x -= 2` ($x = x - 2$), `x *= 3` ($x = x \times 3$), `x /= 2` ($x = x / 2$).

### 4.4 Relational (Comparison) Operators

Comparison operators evaluate conditions and return a boolean (`True` or `False`):
`==` (Equal to), `!=` (Not equal to), `>` (Greater than), `<` (Less than), `>=` (Greater than or equal), `<=` (Less than or equal).
5 == 5

### 4.5 Logical Operators and Short-Circuit Evaluation

* `and`: Returns `True` only if **both** conditions are `True`.
* `or`: Returns `True` if **at least one** condition is `True`.
* `not`: Negates the boolean value (`not True` $\rightarrow `False`).

#### Short-Circuit Mechanics
* In `A and B`: If `A` is `False`, Python immediately returns `False` without evaluating `B`.
* In `A or B`: If `A` is `True`, Python immediately returns `True` without evaluating `B`.

### 4.6 Identity (`is`) and Membership (`in`) Operators

* **Membership (`in`, `not in`):** Checks whether an element exists inside a collection or sequence:
  ```python
  allowed_roles = ["admin", "editor", "moderator"]
  print("admin" in allowed_roles)  # True
  ```
* **Identity (`is`, `is not`):** Checks whether two variables reference the **exact same memory location**:
  ```python
  status = None
  if status is None:  # Idiomatic Python check for None
      print("No status recorded.")
  ```

> [!NOTE]
> **Advanced Text Reference: Bitwise Operators & Precedence Resolution**
> Python also includes bitwise operators (`&` AND, `|` OR, `^` XOR, `~` NOT, `<<` Left Shift, `>>` Right Shift) used in hardware communication and binary serialization. Python resolves expressions using a strict precedence hierarchy: Parentheses $\rightarrow$ Exponents $\rightarrow$ Unary $\rightarrow$ Multiplication/Division $\rightarrow$ Addition/Subtraction $\rightarrow$ Comparisons/Identity/Membership $\rightarrow$ Logical NOT $\rightarrow$ Logical AND $\rightarrow$ Logical OR.

---

### 4.7 Module 4 Code Skeleton Exam

**Objective:** Complete the discount eligibility expression where a user qualifies for a promotional discount if they are a VIP member OR have a cart total $\ge \$100$, provided their account is active.

```python
# ==========================================
# MODULE 4 EXAM: ELIGIBILITY CHECKER SKELETON
# ==========================================

cart_total = 120.50
is_vip = False
account_active = True

# TODO 1: Complete the logical condition using parentheses, 'and', and 'or'
qualifies_for_discount = ________ and (________ or cart_total >= ________)

# TODO 2: Check if an item is present in inventory
inventory = ["laptop", "mouse", "keyboard", "monitor"]
searched_item = "mouse"

is_in_stock = searched_item ________ inventory

print(f"User Discount Eligibility: {qualifies_for_discount}")  # Expected: True
print(f"Item '{searched_item}' in stock: {is_in_stock}")       # Expected: True
```

<details>
<summary><b>View Solution</b></summary>

```python
cart_total = 120.50
is_vip = False
account_active = True

qualifies_for_discount = account_active and (is_vip or cart_total >= 100.0)

inventory = ["laptop", "mouse", "keyboard", "monitor"]
searched_item = "mouse"

is_in_stock = searched_item in inventory

print(f"User Discount Eligibility: {qualifies_for_discount}")
print(f"Item '{searched_item}' in stock: {is_in_stock}")
```
</details>

---

## 5. Working with Strings & Text Manipulation

### 5.1 String Creation and Quotes

```python
single_q = 'Single quotes allow "embedded" double quotes'
double_q = "Double quotes allow 'embedded' single quotes"
multi_line = """Triple quotes span
across 'multiple' lines seamlessly."""
```

### 5.2 Indexing and Slicing Mechanics

Strings are 0-indexed. Negative indices count backward from the end:
word = "Python"
```text
 Index:   0   1   2   3   4   5
 Char:    P   y   t   h   o   n
-Index:  -6  -5  -4  -3  -2  -1
```

* **Syntax:** `string[start : stop : step]` (Stop index is non-inclusive)

```python
word = "Python"
print(word[0])     # 'P' print()
print(word[-1])    # 'n'
print(word[0:4])   # 'Pyth'
print(word[:2])    # 'Py' (from index 0 up to 2)
print(word[2:])    # 'thon' (from index 2 to end)
print(word[::2])   # 'Pto' (every 2nd character)
print(word[::-1])  # 'nohtyP' (Reversed string)
print(word[-1:])
```

### 5.3 String Immutability

Strings in Python cannot be modified in place:

```python
lang = "Cython"
# lang[0] = "P"  # ❌ Raises TypeError: 'str' object does not support item assignment

# ✅ Create a new modified string:
lang = "P" + lang[1:]
print(lang)  # "Python"
```

### 5.4 Essential String Methods

String methods return **new** modified strings (original is untouched):

```python
raw_text = "   Cloud Server Production 01   "

# 1. Casing
print(raw_text.lower())         # "   cloud server production 01   "
print(raw_text.upper())         # "   CLOUD SERVER PRODUCTION 01   "
print(raw_text.title())         # "   Cloud Server Production 01   "

# 2. Sanitization
clean_text = raw_text.strip()   # "Cloud Server Production 01"

# 3. Search and Inspect
print(clean_text.startswith("Cloud"))  # True
print(clean_text.endswith("01"))       # True
print(clean_text.find("Server"))       # 6 (Index where substring starts)

# 4. Replacement & Splitting
replaced = clean_text.replace("Production", "Staging")
tokens = clean_text.split(" ")  # ['Cloud', 'Server', 'Production', '01']
rejoined = "-".join(tokens)     # "Cloud-Server-Production-01"
```

### 5.5 Formatted String Literals (f-strings)

Introduced in Python 3.6, **f-strings** offer clean, high-performance string formatting:

```python
name = "Database Server"
uptime_pct = 99.9845
port = 5432

print(f"Service:  {name} | Port: {port:05d} | Uptime: {uptime_pct:.2f}%")
# Service: Database Server | Port: 05432 | Uptime: 99.98%
```

### 5.6 Escape Sequences and Raw Strings

* `\n`: Newline | `\t`: Tab | `\\`: Literal backslash | `\"`: Double quote
* **Raw Strings (`r"..."`):** Disables escape parsing (essential for regular expressions and Windows directory paths like `r"C:\Users\Admin\Docs"`).

---

### 5.7 Module 5 Code Skeleton Exam

**Objective:** Complete the string parser that takes a URL string, verifies that it starts with `"https://www.google.com"`, and extracts the domain name and file extension.

```python
# ==========================================
# MODULE 5 EXAM: URL PARSER SKELETON
# ==========================================

url = "https://downloads.python.org/documentation/guide.pdf"

# TODO 1: Verify the URL starts with "https://"
is_secure = url.________("https://")

# TODO 2: Strip off the protocol "https://" prefix
without_protocol = url.replace("https://", "")

# TODO 3: Extract domain name (everything before the first '/')
domain = without_protocol.split("/")[________]

# TODO 4: Extract file extension from the end using .split(".")
file_extension = url.split(".")[-1]

print(f"Secure: {is_secure} | Domain: {domain} | File Type: {file_extension}")
# Expected Output: Secure: True | Domain: downloads.python.org | File Type: pdf
```

<details>
<summary><b>View Solution</b></summary>

```python
url = "https://downloads.python.org/documentation/guide.pdf"

is_secure = url.startswith("https://")
without_protocol = url.replace("https://", "")
domain = without_protocol.split("/")[0]
file_extension = url.split(".")[-1]

print(f"Secure: {is_secure} | Domain: {domain} | File Type: {file_extension}")
```
</details>

---

## 6. Control Flow: Conditional Decision Making

### 6.1 The `if`, `elif`, and `else` Statements

Conditionals allow your program to execute different branches of logic based on evaluated boolean expressions:

```python

bulb_status = "On"

if bulb_status == "On":
    print("Your bulb is on")
else:
    print("Bulb is off")


status_code = 404

if status_code == 200:
    print("OK: Request succeeded.")
elif status_code == 401:
    print("Unauthorized: Authentication required.")
elif status_code == 404:
    print("Not Found: Resource does not exist.")
elif status_code >= 500:
    print("Server Error: Remote host failure.")
else:
    print(f"Unhandled HTTP Status: {status_code}")
```

### 6.2 Nested Conditionals

Conditionals can be placed inside parent conditional blocks:

```python
user_authenticated = True
user_role = "Admin"

if user_authenticated:
    if user_role == "Admin":
        print("Access granted: Full Administrative Dashboard.")
    else:
        print("Access granted: Standard User View.")
else:
    print("Access denied: Please authenticate.")
```
### classwork:  write a python if else statement that checks if a purchase has a discount or not. If it has a discount create another check for quantity. if quantity is greater than 6 print "Discount does not apply, pay full fee". Otherwise the user should pay the normal fee.

### 6.3 Truthy and Falsy Evaluations

In Python, every object has an inherent boolean truth value:

```text
┌───────────────────────────────────────┬───────────────────────────────────────┐
│             Falsy Values              │             Truthy Values             │
├───────────────────────────────────────┼───────────────────────────────────────┤
│ • `False`                             │ • `True`                              │
│ • `None`                              │ • Any non-zero number (`1`, `-2.5`)   │
│ • Zero (`0`, `0.0`, `0j`)             │ • Non-empty string (`"hello"`, `" "`) │
│ • Empty sequences (`""`, `[]`, `()`)  │ • Non-empty list (`[0]`, `[None]`)    │
│ • Empty collections (`set()`, `{}`)   │ • Non-empty dictionary (`{"a": 1}`)   │
└───────────────────────────────────────┴───────────────────────────────────────┘
```

```python
# Clean, idiomatic truthiness check
task_queue = []

if not task_queue:
    print("Queue is currently empty.")
```

### 6.4 Conditional Expressions (Ternary Operator)

A concise one-line syntax for assigning values based on a condition:
`result = value_if_true if condition else value_if_false`

```python
score = 85
status = "Pass" if score >= 70 else "Needs Improvement"
print("Academic Status:", status)  # "Pass"
```

> [!NOTE]
> **Advanced Text Reference: Structural Pattern Matching & Guard Clauses**
> Python 3.10 introduced **Structural Pattern Matching** (`match...case`), allowing pattern decomposition over sequences, dictionaries, and class instances. In software engineering, **Guard Clauses** (early returns on error conditions) are preferred over deep nested conditional trees.

---

### 6.5 Module 6 Code Skeleton Exam

**Objective:** Complete the script to classify temperature readings into safety alert levels.

```python
# MODULE 6 EXAM: TEMPERATURE SAFETY SKELETON

sensor_temp_c = 78.5

# TODO 1: Implement multi-branch conditional classification
# Critical: >= 80.0 | Warning: 65.0 to 79.9 | Normal: 20.0 to 64.9 | Cold: < 20.0
if sensor_temp_c >= 80.0:
    alert_level = "CRITICAL"
    action_required = True
elif sensor_temp_c >= ________:
    alert_level = "WARNING"
    action_required = True
elif sensor_temp_c >= ________:
    alert_level = "NORMAL"
    action_required = False
else:
    alert_level = "COLD"
    action_required = False

# TODO 2: Format status string using ternary operator
action_msg = "IMMEDIATE ACTION NEEDED" ________ action_required ________ "OPERATING NOMINAL"

print(f"Temperature: {sensor_temp_c}°C | Alert: {alert_level} | System: {action_msg}")
# Expected: Alert: WARNING | System: IMMEDIATE ACTION NEEDED
```

<details>
<summary><b>View Solution</b></summary>

```python
sensor_temp_c = 78.5

if sensor_temp_c >= 80.0:
    alert_level = "CRITICAL"
    action_required = True
elif sensor_temp_c >= 65.0:
    alert_level = "WARNING"
    action_required = True
elif sensor_temp_c >= 20.0:
    alert_level = "NORMAL"
    action_required = False
else:
    alert_level = "COLD"
    action_required = False

action_msg = "IMMEDIATE ACTION NEEDED" if action_required else "OPERATING NOMINAL"

print(f"Temperature: {sensor_temp_c}°C | Alert: {alert_level} | System: {action_msg}")
```
</details>

---

## 7. Control Flow: Loops & Iteration

### 7.1 The `while` Loop and Infinite Loop Safeguards

A `while` loop executes repeatedly as long as its controlling condition remains `True`:

```python
attempts = 0
max_retries = 3

while attempts < max_retries:
    attempts += 1
    print(f"Connecting to database server (Attempt {attempts}/{max_retries})...")
print("Connection loop finished.")
```

> [!WARNING]
> If the loop condition never changes to `False`, the program will run indefinitely (**infinite loop**). Always ensure loop control variables are updated, or provide an explicit `break` condition. Press `Ctrl+C` in your terminal to terminate a stuck process.

### 7.2 The `for` Loop and the `range()` Function

The `for` loop iterates across sequences (strings, lists, tuples, or generated number ranges):

```python
# range(start, stop, step) - stop is non-inclusive
for i in range(1, 6):
    print(f"Step {i}", end=" ")
print()  # Output: Step 1 Step 2 Step 3 Step 4 Step 5
```

### 7.3 Loop Control: `break`, `continue`, and `pass`

* **`break`:** Terminates the loop immediately and exits.
* **`continue`:** Skips the rest of the current iteration and jumps to the next cycle.
* **`pass`:** A null placeholder statement used when syntax requires a statement but no action is desired.

```python
for num in range(1, 10):
    if num == 3:
        continue  # Skip processing number 3
    if num == 7:
        break     # Stop loop completely upon reaching 7
    print(num, end=" ")  # 1 2 4 5 6
print()
```

### 7.4 The Loop `else` Clause

Python loops support an optional `else` block that executes **only if the loop completes all iterations normally without hitting a `break` statement**:

```python
target_id = 42
ids = [10, 25, 33, 42, 59]

for item in ids:
    if item == target_id:
        print(f"Found target ID: {target_id}")
        break
else:
    print("Target ID was not found in sequence.")
```

### 7.5 Nested Loops and Coordinate Grids

```python
# 2D coordinate grid generator
for row in range(1, 4):
    for col in range(1, 4):
        print(f"({row},{col})", end=" ")
    print()  # Newline after each row
```

### 7.6 Iteration Helpers: `enumerate()` and `zip()`

* **`enumerate(iterable, start=1)`:** Yields `(index, value)` pairs.
* **`zip(*iterables)`:** Iterates through multiple sequences simultaneously.

```python
services = ["Auth", "Database", "Cache"]
ports = [8080, 5432, 6379]

for idx, (service, port) in enumerate(zip(services, ports), start=1):
    print(f"{idx}. {service:<10} running on port {port}")
```

---

### 7.7 Module 7 Code Skeleton Exam

**Objective:** Complete the scanner loop to inspect a list of system transactions, skip transactions below $\$10.00$, terminate the scan if a flagged transaction ID occurs, and tally total valid volume.

```python
# ==========================================
# MODULE 7 EXAM: TRANSACTION SCANNER SKELETON
# ==========================================

transactions = [
    {"id": "TX101", "amount": 45.00, "flagged": False},
    {"id": "TX102", "amount": 5.50,  "flagged": False},  # Too small (< 10)
    {"id": "TX103", "amount": 120.00, "flagged": False},
    {"id": "TX104", "amount": 300.00, "flagged": True},  # FLAGGED: Must stop
    {"id": "TX105", "amount": 85.00, "flagged": False}
]

total_volume = 0.0
processed_count = 0

for tx in transactions:
    # TODO 1: If transaction is flagged, print alert and break loop
    if tx["flagged"]:
        print(f"Security Alert: Suspicious transaction {tx['id']} detected! Halting.")
        ________
        
    # TODO 2: If transaction amount < 10.0, continue to next record
    if tx["amount"] < 10.0:
        ________
        
    # TODO 3: Accumulate amount into total_volume and increment processed_count
    total_volume += tx["amount"]
    processed_count += 1

print(f"Processed: {processed_count} transactions | Total Volume: ${total_volume:.2f}")
# Expected: Processed: 2 transactions | Total Volume: $165.00
```

<details>
<summary><b>View Solution</b></summary>

```python
for tx in transactions:
    if tx["flagged"]:
        print(f"Security Alert: Suspicious transaction {tx['id']} detected! Halting.")
        break
    if tx["amount"] < 10.0:
        continue
    total_volume += tx["amount"]
    processed_count += 1

print(f"Processed: {processed_count} transactions | Total Volume: ${total_volume:.2f}")
```
</details>

---

## 8. Data Collections: Lists, Tuples, Sets & Dictionaries

### 8.1 Core Collection Comparison Matrix

```text
┌────────────┬─────────────┬───────────┬───────────┬──────────────┬───────────────────────────────┐
│ Collection │ Syntax      │ Ordered?  │ Mutable?  │ Duplicates?  │ Primary Purpose               │
├────────────┼─────────────┼───────────┼───────────┼──────────────┼───────────────────────────────┤
│ List       │ `[1, 2, 3]` │ Yes       │ Yes       │ Yes          │ Sequential collections, queues│
│ Tuple      │ `(1, 2, 3)` │ Yes       │ No        │ Yes          │ Fixed records, coordinates    │
│ Set        │ `{1, 2, 3}` │ No        │ Yes       │ No (Unique)  │ Deduplication, membership math│
│ Dict       │ `{"k": "v"}`│ Yes (3.7+)│ Yes       │ Keys: Unique │ Key-value lookup tables, JSON │
└────────────┴─────────────┴───────────┴───────────┴──────────────┴───────────────────────────────┘
```

### 8.2 Lists (Ordered, Mutable Sequences)

```python
servers = ["web-01", "db-01", "app-01"]

# Adding elements
servers.append("cache-01")       # Adds to end
servers.insert(1, "proxy-01")     # Inserts at index 1
servers.extend(["auth-01", "api-01"]) # Merges sequence

# Removing elements
last_node = servers.pop()        # Removes & returns last item
servers.remove("db-01")          # Removes first matching value
del servers[0]                   # Deletes index 0

# Sorting & reversing
servers.sort()                   # Sorts in-place alphabetically
servers.reverse()                # Reverses in-place
print("Configured Nodes:", servers)
```

### 8.3 Tuples (Ordered, Immutable Sequences)

Tuples guarantee that data cannot be modified after instantiation:

```python
# Creation & single-item tuple trailing comma
point_3d = (10, 20, 30)
single_item = ("constant_key",)

# Tuple Unpacking
x, y, z = point_3d
print(f"X: {x}, Y: {y}, Z: {z}")
```

### 8.4 Sets (Unordered, Unique Collections)

Sets store unique, unordered elements and perform fast membership checking:

```python
# Creation (Empty set MUST use set(), because {} creates an empty dict)
dev_skills = {"Python", "Git", "SQL", "Python"}
print(dev_skills)  # {'Python', 'Git', 'SQL'} (Duplicates dropped)

dev_skills.add("Docker")
dev_skills.discard("Java")  # Safely removes without error if missing

# Mathematical Set Operations
frontend = {"HTML", "CSS", "JS", "TypeScript"}
backend = {"Python", "SQL", "Docker", "JS"}

print(frontend | backend)  # Union: All unique items across both sets
print(frontend & backend)  # Intersection: Items present in BOTH ({'JS'})
print(frontend - backend)  # Difference: Items in frontend but not backend
```

### 8.5 Dictionaries (Key-Value Hash Maps)

Dictionaries map unique keys to arbitrary values:

```python
server_config = {
    "host": "127.0.0.1",
    "port": 8000,
    "ssl": True
}

# Accessing
print(server_config["host"])                      # Direct lookup: "127.0.0.1"
print(server_config.get("timeout", 30))           # Safe lookup with default: 30

# Mutating & Adding
server_config["port"] = 8443                      # Update existing key
server_config["environment"] = "Production"       # Insert new key

# Dictionary Iteration
for key, value in server_config.items():
    print(f"{key:<12} => {value}")
```

### 8.6 List, Set, and Dictionary Comprehensions

Declarative, readable expressions for transforming collections:

```python
# 1. List Comprehension: [expression for item in iterable if condition]
numbers = [1, 2, 3, 4, 5, 6]
even_squares = [n ** 2 for n in numbers if n % 2 == 0]  # [4, 16, 36]

# 2. Set Comprehension
unique_lengths = {len(word) for word in ["apple", "pear", "banana", "apple"]} # {4, 5, 6}

# 3. Dictionary Comprehension
price_map = {"apple": 1.20, "banana": 0.80, "cherry": 2.50}
discounted_prices = {k: v * 0.9 for k, v in price_map.items()}
```

> [!NOTE]
> **Advanced Text Reference: Specialized Collections & Algorithmic Complexity (Big-O)**
> Python's standard `collections` module provides specialized tools: `deque` (fast $O(1)$ pops/appends from both ends for queues), `Counter` (frequency multisets), and `defaultdict` (automatic missing key factory). Lookups in Dictionaries and Sets are $O(1)$ average time complexity via hash tables, whereas Lists require $O(N)$ linear scans for membership tests (`item in list`).

---

### 8.7 Module 8 Code Skeleton Exam

**Objective:** Complete the word frequency and category aggregator skeleton.

```python
# ==========================================
# MODULE 8 EXAM: WORD FREQUENCY SKELETON
# ==========================================

raw_text = "python is clean python is readable and python is powerful"
words = raw_text.split()

word_counts = {}

# TODO 1: Populate word_counts using .get(key, 0)
for w in words:
    word_counts[w] = word_counts.________(w, 0) + 1

# TODO 2: Create a list of words that appear more than once using comprehension
frequent_words = [word for word, count in word_counts.________() if count > 1]

# TODO 3: Create a set of all unique word lengths
unique_lengths = {________(w) for w in words}

print("Word Frequencies:", word_counts)
print("Frequent Words (count > 1):", frequent_words)
print("Unique Word Lengths:", unique_lengths)
# Expected Frequencies: {'python': 3, 'is': 3, 'clean': 1, 'readable': 1, 'and': 1, 'powerful': 1}
```

<details>
<summary><b>View Solution</b></summary>

```python
raw_text = "python is clean python is readable and python is powerful"
words = raw_text.split()

word_counts = {}
for w in words:
    word_counts[w] = word_counts.get(w, 0) + 1

frequent_words = [word for word, count in word_counts.items() if count > 1]
unique_lengths = {len(w) for w in words}

print("Word Frequencies:", word_counts)
print("Frequent Words (count > 1):", frequent_words)
print("Unique Word Lengths:", unique_lengths)
```
</details>

---

## 9. Functions, Modular Design & Scope

### 9.1 Defining and Invoking Functions

Functions are named, reusable code blocks that perform a specific task, promoting the **DRY (Don't Repeat Yourself)** principle:

```python
# Function Definition
def calculate_net_salary(gross: float, tax_rate: float = 0.15) -> float:
    """Calculate net salary after flat tax deduction."""
    return gross * (1 - tax_rate)

# Function Invocation
payout = calculate_net_salary(5000.0, 0.08)
print(f"Monthly Payout: ${payout:.2f}")
```

### 9.2 Parameters vs. Arguments

* **Parameter:** The variable declared in the function signature header.
* **Argument:** The actual concrete value passed during invocation.

### 9.3 Positional, Keyword, and Default Arguments

```python
def configure_endpoint(host, port=8080, ssl=True):
    return f"https://{host}:{port}" if ssl else f"http://{host}:{port}"


# Positional invocation
print(configure_endpoint("localhost"))

# Keyword invocation (order independent)
print(configure_endpoint(port=9000, ssl=False, host="192.168.1.5"))
```

> [!CAUTION]
> **Mutable Default Argument Trap:** Default parameter values are evaluated once when the function is defined, NOT each time it is called. Never use mutable objects (`[]`, `{}`) as defaults. Use `None` as the sentinel default value:
> ```python
> # ✅ Correct Pattern:
> def append_log(message, log_list=None):
>     if log_list is None:
>         log_list = []
>     log_list.append(message)
>     return log_list
> ```

### 9.4 Variable-Length Arguments (`*args` and `**kwargs`)

* `*args`: Gathers excess positional arguments into a **tuple**.
* `**kwargs`: Gathers excess keyword arguments into a **dictionary**.

```python
def log_telemetry(service_name, *metrics, **metadata):
    print(f"Service: {service_name}")
    print(f"Metrics: {metrics}")
    print(f"Metadata: {metadata}")

log_telemetry("AuthService", 45.2, 88.0, region="us-east", version="2.1")
```

### 9.5 Return Values and Multiple Return Unpacking

Functions terminate immediately upon executing a `return` statement. Returning multiple values bundles them into a tuple:

```python
def get_min_max_avg(numbers):
    if not numbers:
        return 0, 0, 0.0
    return min(numbers), max(numbers), sum(numbers) / len(numbers)

low, high, avg = get_min_max_avg([12, 45, 67, 89, 23])
print(f"Min: {low} | Max: {high} | Avg: {avg:.2f}")
```

### 9.6 Variable Scope and the LEGB Hierarchy

Python resolves variable names using the **LEGB** lookup order:

```text
┌────────────────────────────────────────────────────────┐
│ Local (L): Variables declared inside current function  │
├────────────────────────────────────────────────────────┤
│ Enclosing (E): Variables in outer enclosing functions  │
├────────────────────────────────────────────────────────┤
│ Global (G): Variables defined at top module level      │
├────────────────────────────────────────────────────────┤
│ Built-in (B): Predefined names (print, len, range)     │
└────────────────────────────────────────────────────────┘
```

### 9.7 Docstrings (PEP 257) and Type Hints

```python
def convert_celsius_to_fahrenheit(celsius: float) -> float:
    """
    Convert a temperature value from Celsius to Fahrenheit.

    Parameters:
        celsius (float): Temperature in degrees Celsius.

    Returns:
        float: Temperature in degrees Fahrenheit.
    """
    return (celsius * 9/5) + 32
```

> [!NOTE]
> **Advanced Text Reference: Closures, Decorators & Positional-Only Boundaries**
> In Python, functions are **first-class objects** that can be passed as arguments and returned dynamically. A **Closure** retains access to enclosing variables after outer execution. A **Decorator** (`@wraps`) dynamically wraps functions to add logging, benchmarking, or retry logic. Python 3.8+ also supports positional-only (`/`) and keyword-only (`*`) parameter boundaries (`def api(pos_only, /, standard, *, kw_only):`).

---

### 9.8 Module 9 Code Skeleton Exam

**Objective:** Complete the statistical summary helper function that accepts any number of numeric values via `*args` and returns count, sum, and average.

```python
# ==========================================
# MODULE 9 EXAM: STATS CALCULATOR SKELETON
# ==========================================

def calculate_stats(*numbers: float) -> tuple:
    """Calculate (count, total_sum, average) for arbitrary arguments."""
    # TODO 1: Guard clause: if numbers is empty, return (0, 0.0, 0.0)
    if not numbers:
        return (0, 0.0, 0.0)
        
    # TODO 2: Calculate count, total_sum, and average
    count = ________(numbers)
    total_sum = ________(numbers)
    average = total_sum / ________
    
    # TODO 3: Return the three values as a tuple
    return count, total_sum, average


# Verification Calls:
c, s, a = calculate_stats(10.0, 20.0, 30.0, 40.0)
print(f"Count: {c} | Sum: {s:.2f} | Average: {a:.2f}")
# Expected: Count: 4 | Sum: 100.00 | Average: 25.00
```

<details>
<summary><b>View Solution</b></summary>

```python
def calculate_stats(*numbers: float) -> tuple:
    if not numbers:
        return (0, 0.0, 0.0)
        
    count = len(numbers)
    total_sum = sum(numbers)
    average = total_sum / count
    
    return count, total_sum, average

c, s, a = calculate_stats(10.0, 20.0, 30.0, 40.0)
print(f"Count: {c} | Sum: {s:.2f} | Average: {a:.2f}")
```
</details>

---

## 10. Error Handling & Exception Safety

### 10.1 Syntax Errors vs. Runtime Exceptions

* **Syntax Error:** Grammatical violations of Python syntax. Code cannot be parsed and will not begin execution.
* **Runtime Exception:** Occurs while the syntactically valid program is running (e.g., dividing by zero, missing file, invalid numeric text).

### 10.2 Common Built-in Exceptions

| Exception | Raised When... |
| :--- | :--- |
| `ValueError` | A function receives an argument of right type but invalid value (e.g., `int("abc")`). |
| `TypeError` | An operation is applied to an incompatible data type (e.g., `"10" + 5`). |
| `ZeroDivisionError` | Dividing or modulo-ing any number by zero. |
| `IndexError` | Attempting to access an index out of list sequence range. |
| `KeyError` | Attempting to access a dictionary key that does not exist. |
| `FileNotFoundError` | Attempting to read a file pathway that cannot be found on disk. |

### 10.3 Handling Exceptions with `try`, `except`, `else`, and `finally`

```python
def safe_divide():
    try:
        n1 = float(input("Enter numerator: "))
        n2 = float(input("Enter denominator: "))
        result = n1 / n2
    except ValueError:
        print("Input Error: Both inputs must be valid numeric values.")
    except ZeroDivisionError:
        print("Math Error: Cannot divide by zero.")
    except Exception as e:
        print(f"Unexpected error: {e}")
    else:
        # Executes ONLY if NO errors were raised in the try block
        print(f"Calculation Result: {result:.4f}")
    finally:
        # ALWAYS executes regardless of outcome (used for cleanup)
        print("Calculation session ended.")
```

### 10.4 Raising Custom Exceptions with `raise`

```python
def validate_age(age: int):
    if age < 0:
        raise ValueError("Age cannot be negative.")
    if age > 130:
        raise ValueError("Age exceeds maximum realistic lifespan.")
    return True
```

---

### 10.5 Module 10 Code Skeleton Exam

**Objective:** Complete the robust integer input prompt function that continually prompts the user until a valid integer within a given range is entered.

```python
# ==========================================
# MODULE 10 EXAM: ROBUST PROMPT SKELETON
# ==========================================

def get_bounded_integer(prompt: str, min_val: int, max_val: int) -> int:
    """Repeatedly prompts user for an integer between min_val and max_val."""
    while True:
        try:
            # TODO 1: Read input and cast to int
            val = ________(input(prompt))
            
            # TODO 2: Validate boundaries
            if val < min_val or val > max_val:
                print(f"⚠️ Value must be between {min_val} and {max_val}.")
                ________  # Continue loop
                
            return val  # Successfully parsed and validated
            
        except ________:
            # TODO 3: Catch ValueError when string cannot be converted
            print("⚠️ Invalid format! Please type a whole number.")

# Test simulation:
user_rating = get_bounded_integer("Rate service (1-5): ", 1, 5)
print("Confirmed Rating:", user_rating)
```

<details>
<summary><b>View Solution</b></summary>

```python
def get_bounded_integer(prompt: str, min_val: int, max_val: int) -> int:
    while True:
        try:
            val = int(input(prompt))
            if val < min_val or val > max_val:
                print(f"⚠️ Value must be between {min_val} and {max_val}.")
                continue
            return val
        except ValueError:
            print("⚠️ Invalid format! Please type a whole number.")
```
</details>

---

## 11. File I/O & Structured Data Handling

### 11.1 File Access Modes

| Mode | Name | Description |
| :---: | :--- | :--- |
| `'r'` | Read (Default) | Opens for reading. Raises `FileNotFoundError` if missing. |
| `'w'` | Write | Creates new file or **overwrites** existing file content. |
| `'a'` | Append | Writes new data at the **end** of file without overwriting. |
| `'x'` | Exclusive Creation | Creates new file; fails if file already exists. |

### 11.2 The `with` Statement (Context Managers)

Always open files using `with`. It deterministically closes the file stream when the block exits, even if exceptions occur:

```python
# Idiomatic File I/O
with open("system.log", "w", encoding="utf-8") as f:
    f.write("[INFO] Application started.\n")
    f.write("[INFO] Database connected.\n")
# File handle is closed safely here automatically
```

### 11.3 Reading and Writing Plain Text Files

```python
# 1. Reading line-by-line (Memory efficient for large files)
with open("system.log", "r", encoding="utf-8") as f:
    for line_number, line in enumerate(f, start=1):
        print(f"Line {line_number}: {line.strip()}")
```

### 11.4 Working with CSV Data (`csv` Module)

```python
import csv

records = [
    {"username": "asmith", "role": "admin", "active": "True"},
    {"username": "bjones", "role": "developer", "active": "True"}
]

# Writing CSV using DictWriter
with open("users.csv", "w", newline="", encoding="utf-8") as f:
    fieldnames = ["username", "role", "active"]
    writer = csv.DictWriter(f, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(records)

# Reading CSV using DictReader
with open("users.csv", "r", encoding="utf-8") as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(f"User: {row['username']} | Role: {row['role']}")
```

### 11.5 Working with JSON Data (`json` Module)

JSON is the standard format for Web APIs and configuration files:

```python
import json

app_state = {
    "version": "1.4.0",
    "theme": "dark",
    "max_connections": 100
}

# Serialization: Dict -> JSON File
with open("config.json", "w", encoding="utf-8") as f:
    json.dump(app_state, f, indent=4)

# Deserialization: JSON File -> Dict
with open("config.json", "r", encoding="utf-8") as f:
    loaded_state = json.load(f)
    print("Loaded Version:", loaded_state["version"])
```

> [!NOTE]
> **Advanced Text Reference: Databases (SQLite), Pathlib & Desktop GUI Systems**
> Beyond text/JSON files, Python includes `sqlite3` for relational database storage with SQL schemas, transactions (`commit()` / `rollback()`), and parameterized queries to prevent SQL injection. Cross-platform filesystem navigation is managed with `pathlib.Path`. Desktop visual interfaces can be authored with Python's standard `tkinter` library.

---

### 11.6 Module 11 Code Skeleton Exam

**Objective:** Complete the script to read a configuration key-value file, ignore comment lines starting with `#`, and export a parsed JSON file.

```python
# ==========================================
# MODULE 11 EXAM: CONFIG PARSER SKELETON
# ==========================================
import json

raw_config_lines = [
    "# Production Server Config\n",
    "HOST=127.0.0.1\n",
    "PORT=8080\n",
    "\n",
    "# Security\n",
    "SSL_ENABLED=True\n"
]

# Write test file
with open("server.conf", "w", encoding="utf-8") as f:
    f.writelines(raw_config_lines)

parsed_settings = {}

# TODO 1: Read server.conf line-by-line and parse into parsed_settings dict
with open("server.conf", "________", encoding="utf-8") as in_file:
    for line in in_file:
        cleaned = line.________()
        # TODO 2: Skip empty lines or comment lines starting with '#'
        if not cleaned or cleaned.startswith(________):
            continue
        if "=" in cleaned:
            key, val = cleaned.split("=", 1)
            parsed_settings[key.strip()] = val.strip()

# TODO 3: Export parsed_settings dictionary to "server_config.json"
with open("server_config.json", "w", encoding="utf-8") as json_out:
    json.________(parsed_settings, json_out, indent=2)

print("Parsed Settings:", parsed_settings)
# Expected: {'HOST': '127.0.0.1', 'PORT': '8080', 'SSL_ENABLED': 'True'}
```

<details>
<summary><b>View Solution</b></summary>

```python
with open("server.conf", "r", encoding="utf-8") as in_file:
    for line in in_file:
        cleaned = line.strip()
        if not cleaned or cleaned.startswith("#"):
            continue
        if "=" in cleaned:
            key, val = cleaned.split("=", 1)
            parsed_settings[key.strip()] = val.strip()

with open("server_config.json", "w", encoding="utf-8") as json_out:
    json.dump(parsed_settings, json_out, indent=2)

print("Parsed Settings:", parsed_settings)
```
</details>

---

## 12. Modules, Standard Library & Virtual Environments

### 12.1 What is a Module? Import Syntax

A **module** is any `.py` file containing functions and classes. A **package** is a directory of modules.

```python
# Method 1: Import entire module
import math
print(math.sqrt(64))        # 8.0

# Method 2: Import specific members
from math import pi, floor
print(floor(4.9))           # 4

# Method 3: Import with alias
import random as rnd
print(rnd.randint(1, 10))   # Random integer 1-10
```

### 12.2 Standard Library Highlights (`random`, `datetime`, `math`, `sys`)

* `random`: Generating random numbers, shuffling, and choosing items (`random.choice(seq)`).
* `datetime`: Timestamps and date calculations (`datetime.now()`).
* `math`: Trigonometry, logarithms, powers, and constants (`math.pi`).
* `sys`: Python runtime details and system CLI arguments (`sys.argv`).

### 12.3 Creating Custom Modules and `if __name__ == "__main__":`

When Python runs a file directly, it sets `__name__ = "__main__"`. When imported as a module, `__name__` is set to the module name.

```python
# string_helpers.py
def clean_username(name: str) -> str:
    return name.strip().lower()

# Guard block: Only runs when running this file directly, NOT when imported
if __name__ == "__main__":
    print("Testing locally:", clean_username("  AliceSmith  "))
```

### 12.4 Package Management with `pip`

```bash
# Install third-party package
pip install requests

# Freeze project dependencies to requirements file
pip freeze > requirements.txt

# Install all packages from requirements file
pip install -r requirements.txt
```

### 12.5 Virtual Environments (`venv`)

A **virtual environment** isolates project packages so dependencies from different projects do not conflict:

```bash
# 1. Create virtual environment named '.venv'
python -m venv .venv

# 2. Activate virtual environment
# Windows (PowerShell):
.venv\Scripts\Activate.ps1
# Windows (Command Prompt):
.venv\Scripts\activate.bat
# macOS / Linux:
source .venv/bin/activate

# 3. Deactivate when finished
deactivate
```

---

### 12.6 Module 12 Code Skeleton Exam

**Objective:** Create a secure token generator function utilizing the standard `random` and `string` modules.

```python
# ==========================================
# MODULE 12 EXAM: TOKEN GENERATOR SKELETON
# ==========================================
import random
import string

def generate_secure_token(length: int = 16) -> str:
    """Generates a random token containing uppercase, lowercase, and digits."""
    # TODO 1: Validate length is at least 8, else raise ValueError
    if length < 8:
        raise ________("Token length must be at least 8 characters.")
        
    # TODO 2: Combine letters and digits from string module
    allowed_chars = string.ascii_letters + string.________
    
    # TODO 3: Select random characters and join into a string
    token = "".join(random.________(allowed_chars) for _ in range(length))
    return token

# Test call
generated_token = generate_secure_token(16)
print("Generated Security Token:", generated_token)
print("Token Length Verified:", len(generated_token) == 16)
```

<details>
<summary><b>View Solution</b></summary>

```python
def generate_secure_token(length: int = 16) -> str:
    if length < 8:
        raise ValueError("Token length must be at least 8 characters.")
        
    allowed_chars = string.ascii_letters + string.digits
    token = "".join(random.choice(allowed_chars) for _ in range(length))
    return token

generated_token = generate_secure_token(16)
print("Generated Security Token:", generated_token)
print("Token Length Verified:", len(generated_token) == 16)
```
</details>

---

## 13. Introduction to Object-Oriented Programming (OOP)

### 13.1 Core OOP Principles: Classes and Instances

**Object-Oriented Programming (OOP)** organizes software around real-world data (**attributes**) and behaviors (**methods**) modeled as objects.

* **Class:** Blueprint / template (`class BankAccount:`).
* **Object / Instance:** A concrete instance instantiated from the class (`acc1 = BankAccount("Alice", 500)`).

```text
Class Blueprint: BankAccount
┌──────────────────────────────────────┐
│ Attributes: self.holder, self.balance│
│ Methods:    deposit(), withdraw()    │
└──────────────────┬───────────────────┘
                   │ Instantiates
         ┌─────────┴─────────┐
         ▼                   ▼
Object 1: "Alice" ($500)   Object 2: "Bob" ($1200)
```

### 13.2 The `__init__` Constructor and `self`

* `__init__()`: The initializer method called automatically when creating a new instance.
* `self`: Refers to the **current instance** of the object being created or operated upon.

```python
class BankAccount:
    def __init__(self, account_holder: str, initial_balance: float = 0.0):
        self.holder = account_holder
        self.balance = initial_balance

    def deposit(self, amount: float):
        if amount <= 0:
            raise ValueError("Deposit amount must be positive.")
        self.balance += amount
        print(f"Deposited ${amount:.2f}. Balance: ${self.balance:.2f}")
```

### 13.3 Instance Methods vs. Class Attributes

* **Instance Attribute:** Unique to each individual object (`self.holder`).
* **Class Attribute:** Shared across **all** instances of the class (`bank_name = "Global Trust"`).

### 13.4 Object String Representation (`__str__` and `__repr__`)

* `__str__()`: User-facing readable representation (called by `print(obj)`).
* `__repr__()`: Developer debugging representation (called in REPL and logs).

```python
class ServerNode:
    def __init__(self, node_id: str, ip_address: str):
        self.node_id = node_id
        self.ip_address = ip_address

    def __str__(self) -> str:
        return f"Node {self.node_id} ({self.ip_address})"

    def __repr__(self) -> str:
        return f"ServerNode(node_id='{self.node_id}', ip_address='{self.ip_address}')"
```

### 13.5 Basic Inheritance and `super()`

Inheritance allows child classes to reuse and specialize parent class attributes and methods:

```python
class Vehicle:
    def __init__(self, make: str, model: str):
        self.make = make
        self.model = model

    def start(self) -> str:
        return f"{self.make} {self.model} started."

class ElectricCar(Vehicle):
    def __init__(self, make: str, model: str, battery_kwh: int):
        super().__init__(make, model)  # Call parent constructor
        self.battery_kwh = battery_kwh

    def start(self) -> str:
        return f"{self.make} {self.model} powered on silently (Battery: {self.battery_kwh} kWh)."
```

> [!NOTE]
> **Advanced Text Reference: Advanced OOP & Metaprogramming**
> Advanced OOP patterns include `@classmethod` (operating on class level), `@staticmethod` (utility functions), `@property` (custom getters/setters), Abstract Base Classes (`abc.ABC`), and Multiple Inheritance with Method Resolution Order (MRO).

---

### 13.6 Module 13 Code Skeleton Exam

**Objective:** Complete the Bank Account hierarchy with a `SavingsAccount` child class that charges a withdrawal fee if balance falls below a minimum threshold.

```python
# ==========================================
# MODULE 13 EXAM: OOP BANKING SKELETON
# ==========================================

class BankAccount:
    def __init__(self, owner: str, balance: float):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount: float):
        self.balance += amount

    def withdraw(self, amount: float) -> bool:
        if amount <= self.balance:
            self.balance -= amount
            return True
        return False

    def __str__(self) -> str:
        return f"Account[{self.owner}]: ${self.balance:.2f}"


class PremiumSavingsAccount(BankAccount):
    def __init__(self, owner: str, balance: float, interest_rate: float):
        # TODO 1: Invoke parent constructor using super()
        ________.__init__(owner, balance)
        self.interest_rate = interest_rate

    def apply_interest(self):
        # TODO 2: Calculate and add interest to self.balance
        interest = self.balance * self.________
        self.deposit(interest)


# Test Verification
acc = PremiumSavingsAccount("Elena Rostova", 1000.0, 0.05)
acc.deposit(500.0)      # Balance: 1500.0
acc.apply_interest()    # 5% of 1500 = 75.0 -> Balance: 1575.0
print(acc)
# Expected: Account[Elena Rostova]: $1575.00
```

<details>
<summary><b>View Solution</b></summary>

```python
class PremiumSavingsAccount(BankAccount):
    def __init__(self, owner: str, balance: float, interest_rate: float):
        super().__init__(owner, balance)
        self.interest_rate = interest_rate

    def apply_interest(self):
        interest = self.balance * self.interest_rate
        self.deposit(interest)

acc = PremiumSavingsAccount("Elena Rostova", 1000.0, 0.05)
acc.deposit(500.0)
acc.apply_interest()
print(acc)
```
</details>

---

## 14. Comprehensive Capstone Practice Projects

### 14.1 Project 1: Number Guessing Challenge

```python
# project1_guessing_game.py
import random

def run_guessing_game():
    secret_number = random.randint(1, 100)
    max_attempts = 7
    attempts = 0

    print("=" * 45)
    print("🎯 NUMBER GUESSING CHALLENGE (1-100)")
    print(f"You have {max_attempts} attempts to find the secret number.")
    print("=" * 45)

    while attempts < max_attempts:
        attempts += 1
        try:
            guess = int(input(f"\nAttempt {attempts}/{max_attempts} - Enter guess: "))
        except ValueError:
            print("⚠️ Please enter a valid whole number.")
            attempts -= 1
            continue

        if guess == secret_number:
            print(f"\n🎉 Correct! You found the number ({secret_number}) in {attempts} attempts!")
            break
        elif guess < secret_number:
            print("📈 Too Low!")
        else:
            print("📉 Too High!")
    else:
        print(f"\n💀 Game Over! The secret number was {secret_number}.")

if __name__ == "__main__":
    run_guessing_game()
```

---

### 14.2 Project 2: Interactive Console CRUD Task Manager

```python
# project2_task_manager.py

tasks = []

def display_menu():
    print("\n--- 📋 TASK MANAGER ---")
    print("1. View Tasks")
    print("2. Add Task")
    print("3. Complete Task")
    print("4. Delete Task")
    print("5. Exit")

def main():
    while True:
        display_menu()
        choice = input("Select an option (1-5): ").strip()
        
        if choice == "1":
            if not tasks:
                print("ℹ️ No active tasks.")
            for i, t in enumerate(tasks, start=1):
                status = "✅ [DONE]" if t["done"] else "⏳ [PENDING]"
                print(f"{i}. {status} {t['title']}")
                
        elif choice == "2":
            title = input("Enter task description: ").strip()
            if title:
                tasks.append({"title": title, "done": False})
                print("Task added successfully.")
                
        elif choice == "3":
            try:
                idx = int(input("Enter task number to mark complete: "))
                if 1 <= idx <= len(tasks):
                    tasks[idx - 1]["done"] = True
                    print("Task marked complete.")
            except ValueError:
                print("Invalid input.")
                
        elif choice == "4":
            try:
                idx = int(input("Enter task number to delete: "))
                if 1 <= idx <= len(tasks):
                    removed = tasks.pop(idx - 1)
                    print(f"Deleted task: {removed['title']}")
            except ValueError:
                print("Invalid input.")
                
        elif choice == "5":
            print("Exiting Task Manager. Goodbye!")
            break

if __name__ == "__main__":
    main()
```

---

### 14.3 Project 3: Automated Text File Word Frequency Reporter

```python
# project3_word_reporter.py
import string

def generate_word_report(input_file: str, output_file: str):
    counts = {}
    try:
        with open(input_file, "r", encoding="utf-8") as f:
            for line in f:
                clean_line = line.translate(str.maketrans("", "", string.punctuation)).lower()
                for word in clean_line.split():
                    counts[word] = counts.get(word, 0) + 1
    except FileNotFoundError:
        print(f"Error: '{input_file}' not found.")
        return

    sorted_words = sorted(counts.items(), key=lambda item: item[1], reverse=True)

    with open(output_file, "w", encoding="utf-8") as out:
        out.write("WORD FREQUENCY ANALYSIS REPORT\n")
        out.write("=" * 35 + "\n")
        out.write(f"Total Unique Words: {len(sorted_words)}\n\n")
        out.write(f"{'Rank':<6}{'Word':<18}{'Count'}\n")
        out.write("-" * 35 + "\n")
        for rank, (w, c) in enumerate(sorted_words[:10], start=1):
            out.write(f"{rank:<6}{w:<18}{c}\n")

    print(f"✅ Report saved to '{output_file}'.")

if __name__ == "__main__":
    with open("sample.txt", "w", encoding="utf-8") as f:
        f.write("Python is great. Python is readable and Python is practical.")
    generate_word_report("sample.txt", "word_report.txt")
```

---

### 14.4 Project 4: Full OOP Student Gradebook & Report Generator

```python
# project4_gradebook.py

class Student:
    def __init__(self, student_id: str, name: str):
        self.student_id = student_id
        self.name = name
        self.grades = []

    def add_grade(self, grade: float):
        if 0.0 <= grade <= 100.0:
            self.grades.append(grade)
        else:
            raise ValueError("Grade must be between 0 and 100.")

    def get_average(self) -> float:
        return sum(self.grades) / len(self.grades) if self.grades else 0.0

    def get_letter_grade(self) -> str:
        avg = self.get_average()
        if avg >= 90: return "A"
        if avg >= 80: return "B"
        if avg >= 70: return "C"
        if avg >= 60: return "D"
        return "F"

    def __str__(self) -> str:
        return f"[{self.student_id}] {self.name:<20} Avg: {self.get_average():.2f} ({self.get_letter_grade()})"


class GradeBook:
    def __init__(self):
        self.students = {}

    def add_student(self, student_id: str, name: str):
        self.students[student_id] = Student(student_id, name)

    def record_grade(self, student_id: str, grade: float):
        if student_id in self.students:
            self.students[student_id].add_grade(grade)
        else:
            print(f"Error: Student {student_id} not registered.")

    def display_summary(self):
        print("\n" + "=" * 50)
        print("           OFFICIAL GRADEBOOK REPORT")
        print("=" * 50)
        for s in self.students.values():
            print(s)
        
        all_averages = [s.get_average() for s in self.students.values() if s.grades]
        if all_averages:
            class_avg = sum(all_averages) / len(all_averages)
            print("-" * 50)
            print(f"Class Overall Average: {class_avg:.2f}")

if __name__ == "__main__":
    gb = GradeBook()
    gb.add_student("S101", "Alice Smith")
    gb.add_student("S102", "Bob Jones")
    
    gb.record_grade("S101", 95.0)
    gb.record_grade("S101", 88.5)
    gb.record_grade("S102", 76.0)
    gb.record_grade("S102", 82.0)
    
    gb.display_summary()
```

---

## 15. Python Best Practices & Specialization Learning Roadmap

### 15.1 PEP 8 Core Style Standards

1. **Indentation:** Exactly 4 spaces per indentation level.
2. **Naming Conventions:**
   * `snake_case` for variables, attributes, and functions.
   * `PascalCase` for class definitions.
   * `UPPER_CASE` for global constant declarations.
3. **Line Length:** Keep code within 79–88 characters per line.
4. **Imports:** Group standard library imports first, third-party packages second, and local modules third.
5. **Whitespace:** Place single spaces around binary operators (`a = b + c`) and after commas (`[1, 2, 3]`).

### 15.2 Specialization Tracks

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│                          Where to Go From Here?                             │
├───────────────────────┬─────────────────────────────────────────────────────┤
│ 🌐 Web & API Backends │ Learn FastAPI or Django; PostgreSQL, REST APIs,     │
│                       │ Docker containerization, AsyncIO.                   │
├───────────────────────┼─────────────────────────────────────────────────────┤
│ 📊 Data Science & AI  │ Learn NumPy, Pandas, Matplotlib, Scikit-Learn,      │
│                       │ PyTorch, Jupyter Notebooks.                         │
├───────────────────────┼─────────────────────────────────────────────────────┤
│ ⚙️ Automation & Tools │ Learn Playwright/Scrapy (Web Automation), Click or  │
│                       │ Typer (CLI development), OpenPyXL (Spreadsheets).   │
├───────────────────────┼─────────────────────────────────────────────────────┤
│ 🖥️ Desktop & DBs      │ Learn Tkinter/PyQt6 and relational databases with   │
│                       │ SQLite / SQLAlchemy ORM.                            │
└───────────────────────┴─────────────────────────────────────────────────────┘
```

### 15.3 Recommended Next Steps & Resources

* **Official Python Documentation:** [docs.python.org](https://docs.python.org/3/)
* **Practice Portals:** [Exercism.org](https://exercism.org/tracks/python), [LeetCode](https://leetcode.com/)
* **Recommended Next Books:**
  * *Automate the Boring Stuff with Python* by Al Sweigart (Hands-on automation)
  * *Python Crash Course* by Eric Matthes (Project-based learning)
  * *Fluent Python* by Luciano Ramalho (For advancing to professional/idiomatic Python)

---
*Happy Coding! Consistent daily practice of 20–30 minutes builds lasting programming fluency.*
