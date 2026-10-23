# Python Programming: Complete Foundational Reference

A comprehensive, detailed, and structured reference manual covering fundamental to intermediate Python programming concepts.

---

## Table of Contents

- [1. Getting Started](#1-getting-started)
  - [1.1 Overview of Python](#11-overview-of-python)
  - [1.2 Execution Model: Bytecode and the Python Virtual Machine](#12-execution-model-bytecode-and-the-python-virtual-machine)
  - [1.3 Installation and Path Configuration](#13-installation-and-path-configuration)
  - [1.4 Development Environments](#14-development-environments)
  - [1.5 Interactive REPL vs. Script Execution](#15-interactive-repl-vs-script-execution)
  - [1.6 Writing and Executing the First Script](#16-writing-and-executing-the-first-script)
  - [1.7 Section Exercises & Solutions](#17-section-exercises--solutions)
- [2. Core Concepts](#2-core-concepts)
  - [2.1 Anatomy of a Python Script](#21-anatomy-of-a-python-script)
  - [2.2 Variables and Memory Allocation](#22-variables-and-memory-allocation)
  - [2.3 Identifier Naming Rules and Conventions](#23-identifier-naming-rules-and-conventions)
  - [2.4 Comments and Documentation](#24-comments-and-documentation)
  - [2.5 Reserved Keywords](#25-reserved-keywords)
  - [2.6 Code Blocks and Whitespace Indentation](#26-code-blocks-and-whitespace-indentation)
  - [2.7 Console Output with `print()`](#27-console-output-with-print)
  - [2.8 Section Exercises & Solutions](#28-section-exercises--solutions)
- [3. Input Practice](#3-input-practice)
  - [3.1 Mechanics of Standard Input (`input()`)](#31-mechanics-of-standard-input-input)
  - [3.2 String Return Nature and Type Conversion](#32-string-return-nature-and-type-conversion)
  - [3.3 Prompt Engineering and Formatting](#33-prompt-engineering-and-formatting)
  - [3.4 Parsing Multi-Value Input](#34-parsing-multi-value-input)
  - [3.5 Input Sanitization and Basic Validation](#35-input-sanitization-and-basic-validation)
  - [3.6 Practical Interactive CLI Implementations](#36-practical-interactive-cli-implementations)
  - [3.7 Section Exercises & Solutions](#37-section-exercises--solutions)
- [4. Data Types](#4-data-types)
  - [4.1 Numeric Types (`int`, `float`, `complex`)](#41-numeric-types-int-float-complex)
  - [4.2 Boolean Type (`bool`)](#42-boolean-type-bool)
  - [4.3 The None Type (`NoneType`)](#43-the-none-type-nonetype)
  - [4.4 Type Inspection and Type Casting](#44-type-inspection-and-type-casting)
  - [4.5 Text Sequence Type (`str`)](#45-text-sequence-type-str)
  - [4.6 String Indexing and Slicing](#46-string-indexing-and-slicing)
  - [4.7 String Immutability](#47-string-immutability)
  - [4.8 Built-in String Methods](#48-built-in-string-methods)
  - [4.9 Formatted String Literals (f-strings)](#49-formatted-string-literals-f-strings)
  - [4.10 Escape Sequences and Raw Strings](#410-escape-sequences-and-raw-strings)
  - [4.11 Section Exercises & Solutions](#411-section-exercises--solutions)
- [5. Operators](#5-operators)
  - [5.1 Arithmetic Operators](#51-arithmetic-operators)
  - [5.2 Assignment and Augmented Assignment Operators](#52-assignment-and-augmented-assignment-operators)
  - [5.3 Comparison (Relational) Operators](#53-comparison-relational-operators)
  - [5.4 Logical Operators and Short-Circuit Evaluation](#54-logical-operators-and-short-circuit-evaluation)
  - [5.5 Bitwise Operators](#55-bitwise-operators)
  - [5.6 Identity Operators (`is`, `is not`)](#56-identity-operators-is-is-not)
  - [5.7 Membership Operators (`in`, `not in`)](#57-membership-operators-in-not-in)
  - [5.8 Operator Precedence and Associativity](#58-operator-precedence-and-associativity)
  - [5.9 Section Exercises & Solutions](#59-section-exercises--solutions)
- [6. Flow Control](#6-flow-control)
  - [6.1 Conditional Statements (`if`, `elif`, `else`)](#61-conditional-statements-if-elif-else)
  - [6.2 Nested Conditionals and Multi-Branch Logic](#62-nested-conditionals-and-multi-branch-logic)
  - [6.3 Truthy and Falsy Evaluation Rules](#63-truthy-and-falsy-evaluation-rules)
  - [6.4 Conditional Expressions (Ternary Operator)](#64-conditional-expressions-ternary-operator)
  - [6.5 Structural Pattern Matching (`match...case`)](#65-structural-pattern-matching-matchcase)
  - [6.6 Guard Clauses and Branch Cleanliness](#66-guard-clauses-and-branch-cleanliness)
  - [6.7 Section Exercises & Solutions](#67-section-exercises--solutions)
- [7. Loops](#7-loops)
  - [7.1 Definite vs. Indefinite Iteration](#71-definite-vs-indefinite-iteration)
  - [7.2 The `while` Loop and Infinite Loop Prevention](#72-the-while-loop-and-infinite-loop-prevention)
  - [7.3 The `for` Loop and the `range()` Function](#73-the-for-loop-and-the-range-function)
  - [7.4 Loop Control Statements (`break`, `continue`, `pass`)](#74-loop-control-statements-break-continue-pass)
  - [7.5 The Loop `else` Clause](#75-the-loop-else-clause)
  - [7.6 Nested Loops and Coordinate Grids](#76-nested-loops-and-coordinate-grids)
  - [7.7 Iteration Helpers (`enumerate()`, `zip()`, `reversed()`, `sorted()`)](#77-iteration-helpers-enumerate-zip-reversed-sorted)
  - [7.8 Section Exercises & Solutions](#78-section-exercises--solutions)
- [8. Data Structures](#8-data-structures)
  - [8.1 Core Collection Comparison](#81-core-collection-comparison)
  - [8.2 Lists (Ordered, Mutable Sequences)](#82-lists-ordered-mutable-sequences)
  - [8.3 Tuples (Ordered, Immutable Sequences)](#83-tuples-ordered-immutable-sequences)
  - [8.4 Sets (Unordered, Unique Hashable Collections)](#84-sets-unordered-unique-hashable-collections)
  - [8.5 Dictionaries (Key-Value Hash Maps)](#85-dictionaries-key-value-hash-maps)
  - [8.6 Comprehensions (List, Set, Dict, Generator Expressions)](#86-comprehensions-list-set-dict-generator-expressions)
  - [8.7 Specialized Collections (`collections` Module)](#87-specialized-collections-collections-module)
  - [8.8 Algorithmic Complexity (Big-O) Overview](#88-algorithmic-complexity-big-o-overview)
  - [8.9 Section Exercises & Solutions](#89-section-exercises--solutions)
- [9. Functions](#9-functions)
  - [9.1 Modular Architecture and Reusability](#91-modular-architecture-and-reusability)
  - [9.2 Function Definition and Invocation](#92-function-definition-and-invocation)
  - [9.3 Parameters vs. Arguments](#93-parameters-vs-arguments)
  - [9.4 Positional, Keyword, and Default Arguments](#94-positional-keyword-and-default-arguments)
  - [9.5 Variable-Length Arguments (`*args`, `**kwargs`)](#95-variable-length-arguments-args-kwargs)
  - [9.6 Positional-Only (`/`) and Keyword-Only (`*`) Parameters](#96-positional-only--and-keyword-only--parameters)
  - [9.7 Return Values and Multiple Return Unpacking](#97-return-values-and-multiple-return-unpacking)
  - [9.8 Variable Scope and Namespace (LEGB Rule)](#98-variable-scope-and-namespace-legb-rule)
  - [9.9 First-Class Functions and Higher-Order Functions](#99-first-class-functions-and-higher-order-functions)
  - [9.10 Closures and Decorators](#910-closures-and-decorators)
  - [9.11 Docstrings and Type Annotations](#911-docstrings-and-type-annotations)
  - [9.12 Section Exercises & Solutions](#912-section-exercises--solutions)
- [10. Lambda Functions](#10-lambda-functions)
  - [10.1 Concept and Syntax of Anonymous Functions](#101-concept-and-syntax-of-anonymous-functions)
  - [10.2 Comparison: `def` Statements vs. `lambda` Expressions](#102-comparison-def-statements-vs-lambda-expressions)
  - [10.3 Functional Operations (`map()`, `filter()`, `reduce()`)](#103-functional-operations-map-filter-reduce)
  - [10.4 Custom Sorting and Key Functions](#104-custom-sorting-and-key-functions)
  - [10.5 Appropriate Use Cases and Anti-Patterns](#105-appropriate-use-cases-and-anti-patterns)
  - [10.6 Section Exercises & Solutions](#106-section-exercises--solutions)
- [11. File Handling](#11-file-handling)
  - [11.1 File Paths and Cross-Platform Operations (`pathlib`)](#111-file-paths-and-cross-platform-operations-pathlib)
  - [11.2 File Open Modes](#112-file-open-modes)
  - [11.3 Context Managers and the `with` Statement](#113-context-managers-and-the-with-statement)
  - [11.4 Reading Operations](#114-reading-operations)
  - [11.5 Writing and Appending Operations](#115-writing-and-appending-operations)
  - [11.6 File Cursor Management (`tell()`, `seek()`)](#116-file-cursor-management-tell-seek)
  - [11.7 Working with Structured Files (CSV and JSON)](#117-working-with-structured-files-csv-and-json)
  - [11.8 Exception Handling in File I/O](#118-exception-handling-in-file-io)
  - [11.9 Section Exercises & Solutions](#119-section-exercises--solutions)
- [12. SQLite Databases](#12-sqlite-databases)
  - [12.1 Relational Database Principles and SQLite Overview](#121-relational-database-principles-and-sqlite-overview)
  - [12.2 Database Connection and Cursor Architecture](#122-database-connection-and-cursor-architecture)
  - [12.3 Table Creation and Schema Constraints](#123-table-creation-and-schema-constraints)
  - [12.4 Data Manipulation Operations (CRUD)](#124-data-manipulation-operations-crud)
  - [12.5 Parameterized Queries and SQL Injection Prevention](#125-parameterized-queries-and-sql-injection-prevention)
  - [12.6 Transaction Control (Commit, Rollback, Context Managers)](#126-transaction-control-commit-rollback-context-managers)
  - [12.7 Row Factories (`sqlite3.Row`)](#127-row-factories-sqlite3row)
  - [12.8 Complete SQLite Database Manager Module](#128-complete-sqlite-database-manager-module)
  - [12.9 Section Exercises & Solutions](#129-section-exercises--solutions)
- [13. GUI Development](#13-gui-development)
  - [13.1 Desktop GUI Architecture and `tkinter` Overview](#131-desktop-gui-architecture-and-tkinter-overview)
  - [13.2 Application Lifecycle and the Event Loop (`mainloop`)](#132-application-lifecycle-and-the-event-loop-mainloop)
  - [13.3 Core Tkinter & TTK Widgets](#133-core-tkinter--ttk-widgets)
  - [13.4 Geometry Managers (`pack`, `grid`, `place`)](#134-geometry-managers-pack-grid-place)
  - [13.5 State Variables (`StringVar`, `IntVar`, `DoubleVar`, `BooleanVar`)](#135-state-variables-stringvar-intvar-doublevar-booleanvar)
  - [13.6 Event Binding and Callback Mechanisms](#136-event-binding-and-callback-mechanisms)
  - [13.7 Dialogs and Popups (`messagebox`, `filedialog`)](#137-dialogs-and-popups-messagebox-filedialog)
  - [13.8 Object-Oriented GUI Design](#138-object-oriented-gui-design)
  - [13.9 End-to-End Desktop Application Implementation](#139-end-to-end-desktop-application-implementation)
  - [13.10 Section Exercises & Solutions](#1310-section-exercises--solutions)

---

## 1. Getting Started

### 1.1 Overview of Python

Python is an open-source, high-level, interpreted programming language designed with an emphasis on code readability, concise syntax, and rapid application development. Created by Guido van Rossum and initially released in 1991, Python supports multiple programming paradigms, including procedural, object-oriented, and functional programming.

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│                          Core Architectural Traits                          │
├───────────────────┬─────────────────────────────────────────────────────────┤
│ Interpreted       │ Source code is translated into bytecode and executed    │
│                   │ sequentially by an interpreter at runtime.              │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ Dynamically Typed │ Variable types are bound to values at runtime rather   │
│                   │ than explicitly declared during compilation.           │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ Strongly Typed    │ Implicit type coercion is restricted; explicit conversions│
│                   │ are required between incompatible data types.          │
├───────────────────┼─────────────────────────────────────────────────────────┤
│ Cross-Platform    │ Python code executes across Windows, macOS, Linux,      │
│                   │ and embedded systems with identical semantic behavior.  │
└───────────────────┴─────────────────────────────────────────────────────────┘
```

### 1.2 Execution Model: Bytecode and the Python Virtual Machine

Python is not purely interpreted in the raw textual sense. When a script is executed, CPython (the standard reference implementation) follows a two-stage execution lifecycle:

```text
[ Python Source Code (.py) ]
              │
              ▼
    [ Lexer / Parser ] ───► Generates Abstract Syntax Tree (AST)
              │
              ▼
   [ Bytecode Compiler ] ──► Compiles to platform-independent bytecode (.pyc)
              │
              ▼
[ Python Virtual Machine (PVM) ] ──► Evaluates bytecode instructions sequentially
              │
              ▼
     [ Native Machine Code ] ───► CPU Hardware Execution
```

1. **Compilation Step:** The source file (`.py`) is compiled into intermediate, low-level, platform-independent instructions known as **bytecode** (stored in cached `__pycache__/*.pyc` files).
2. **Virtual Machine Step:** The **Python Virtual Machine (PVM)** is the runtime engine that loads and executes bytecode instructions against the underlying host operating system.

### 1.3 Installation and Path Configuration

Python distributions are available from the official repository at [python.org](https://www.python.org/downloads/).

#### Windows Installation
1. Download the latest official 64-bit installer executable.
2. Launch the installer. Check the configuration box labeled **"Add python.exe to PATH"**.
3. Select **"Install Now"** or customize directory pathways as required.

#### Linux / macOS Verification
Most Unix-based operating systems include Python or provide package manager installations:
```bash
# Ubuntu / Debian
sudo apt update && sudo apt install python3 python3-pip python3-venv -y

# macOS via Homebrew
brew install python
```

#### Verifying Environment Setup
Open a command shell (PowerShell, Command Prompt, or Terminal) and issue:
```bash
python --version
# Output: Python 3.12.x (or higher)

pip --version
# Output: pip 24.x from ...
```

### 1.4 Development Environments

Python scripts are plain text files that can be authored in various environments:

| Environment | Classification | Primary Characteristics |
| :--- | :--- | :--- |
| **VS Code** | Code Editor | Lightweight, extensible via the official Python extension, integrated terminal and debugger. |
| **PyCharm** | Dedicated IDE | Full-featured Python IDE with static code analysis, refactoring tools, and test runners. |
| **IDLE** | Bundled IDE | Minimal development environment installed standard with Python distributions. |
| **Terminal Shell** | CLI Tooling | Direct execution via command-line interfaces (`nano`, `vim`, shell runners). |

### 1.5 Interactive REPL vs. Script Execution

Python provides two primary execution modes:

- **Interactive REPL (Read-Eval-Print Loop):** Invoked by typing `python` in a terminal without parameters. Evaluates expressions immediately. Ideal for experimentation, inspecting objects, and testing one-line expressions. Exit via `exit()` or `Ctrl+Z` (Windows) / `Ctrl+D` (Unix).
- **Script Files (`.py`):** Standalone text files containing complete program logic executed sequentially by the interpreter from the command line:
  ```bash
  python script_name.py
  ```

### 1.6 Writing and Executing the First Script

Create a file named `hello_world.py` and input the following content:

```python
# hello_world.py
# Basic demonstration of standard output

print("System initialized.")
print("Python runtime version verified.")
```

Execute the script via the command line:
```bash
python hello_world.py
```

*Console Output:*
```text
System initialized.
Python runtime version verified.
```

### 1.7 Section Exercises & Solutions

#### Exercise 1.1: System Info Display
Create a Python script that outputs a three-line summary containing the programming language name, standard file extension, and primary execution engine.

<details>
<summary><b>View Solution</b></summary>

```python
print("Language: Python")
print("File Extension: .py")
print("Execution Engine: CPython / PVM")
```
</details>

---

## 2. Core Concepts

### 2.1 Anatomy of a Python Script

A Python script consists of instructions evaluated top-to-bottom. Standard components include module imports, constant declarations, function/class definitions, and executable statements.

```python
# 1. Imports
import math

# 2. Constant Declarations (PEP 8 naming: UPPER_CASE)
PI_APPROXIMATION = 3.14159

# 3. Executable Statements
radius = 5.0
calculated_area = PI_APPROXIMATION * (radius ** 2)
print("Computed Area:", calculated_area)
```

### 2.2 Variables and Memory Allocation

In Python, a variable is not a static memory container that holds raw bytes. Instead, a variable is a **symbolic reference (pointer)** bound to an object in memory.

```text
Variable Name (Stack/Namespace)        Object in Heap Memory
┌─────────────────────────────┐        ┌────────────────────────────┐
│         item_count          │ ─────► │ Type: int                  │
│                             │        │ Value: 42                  │
│                             │        │ Reference Count: 1         │
└─────────────────────────────┘        └────────────────────────────┘
```

When reassignment occurs, the reference is rebound to a new object:
```python
x = 10       # x references an integer object with value 10
x = "active" # x now references a string object; the previous integer is subject to garbage collection
```

### 2.3 Identifier Naming Rules and Conventions

Identifiers are names assigned to variables, functions, classes, and modules.

```text
┌───────────────────────────────────────┬───────────────────────────────────────┐
│           Syntactic Rules             │      PEP 8 Style Conventions          │
├───────────────────────────────────────┼───────────────────────────────────────┤
│ • Must begin with a letter (a-z, A-Z) │ • Variables and functions:            │
│   or an underscore (`_`).             │   snake_case (e.g., total_revenue)    │
│ • Cannot start with a numeric digit.  │ • Classes:                            │
│ • Can contain alphanumeric characters  │   PascalCase (e.g., DatabaseManager)  │
│   and underscores (`_`).              │ • Constants:                          │
│ • Case-sensitive (`value` != `Value`).│   UPPER_CASE (e.g., MAX_BUFFER_SIZE)  │
│ • Cannot collide with keywords.       │ • Protected attributes: `_single_lead`│
└───────────────────────────────────────┴───────────────────────────────────────┘
```

### 2.4 Comments and Documentation

Comments provide contextual explanations for code logic and are ignored by the parser.

```python
# Single-line comment explaining why a formula is used

tax_rate = 0.08  # Inline comment describing this specific parameter

"""
Multi-line block comment.
Often used for high-level module documentation
or temporarily disabling blocks of logic during development.
"""
```

### 2.5 Reserved Keywords

Python reserves 35 keywords that cannot be used as identifiers. They form the fundamental grammar of the language:

```text
False      await      else       import     pass
None       break      except     in         raise
True       class      finally    is         return
and        continue   for        lambda     try
as         def        from       nonlocal   while
assert     del        global     not        with
async      elif       if         or         yield
```

Keywords can be inspected programmatically:
```python
import keyword
print(keyword.kwlist)
```

### 2.6 Code Blocks and Whitespace Indentation

Python enforces block structure through **whitespace indentation** rather than curly braces `{}` or `begin/end` statements.

- The standard indentation level is **4 spaces** per block depth.
- Inconsistent mixing of tabs and spaces raises an `IndentationError` or `TabError`.

```python
threshold = 100
current_value = 150

if current_value > threshold:
    # Indented block begins (Level 1: 4 spaces)
    status_flag = True
    print("Threshold exceeded.")
    if status_flag:
        # Nested block begins (Level 2: 8 spaces)
        print("Alert triggered.")

# Unindented statement (Level 0: executed sequentially)
print("Evaluation complete.")
```

### 2.7 Console Output with `print()`

The built-in `print()` function sends formatted text to standard output (`sys.stdout`).

```python
# Function Signature:
# print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)

# Custom separator between multiple arguments
print("2026", "09", "28", sep="-")
# Output: 2026-09-28

# Custom line termination
print("Connecting", end="...")
print("Established")
# Output: Connecting...Established
```

### 2.8 Section Exercises & Solutions

#### Exercise 2.1: Variable Binding and Formatting
Define three variables representing a system service: `service_name` (string), `port_number` (integer), and `is_running` (boolean). Print these values formatted on a single line separated by vertical pipes (`|`).

<details>
<summary><b>View Solution</b></summary>

```python
service_name = "AuthService"
port_number = 8080
is_running = True

print(service_name, port_number, is_running, sep=" | ")
```
</details>

---

## 3. Input Practice

### 3.1 Mechanics of Standard Input (`input()`)

The built-in `input()` function pauses script execution, displays an optional prompt string to standard output, and reads a line of text from standard input (`sys.stdin`) until a newline character (`\n`) is encountered.

```python
received_data = input("Enter identification string: ")
print("Stored value:", received_data)
```

### 3.2 String Return Nature and Type Conversion

The `input()` function **always returns a value of type `str`**, regardless of whether the user inputs numbers, text, or punctuation.

```python
# Direct arithmetic on raw input results in string concatenation or TypeError:
val1 = input("Enter first number: ")   # User types 10 -> val1 is "10"
val2 = input("Enter second number: ")  # User types 20 -> val2 is "20"
print(val1 + val2)                     # Result is "1020" (Concatenation)

# Correct approach: Explicit type casting
num1 = int(input("Enter first integer: "))
num2 = float(input("Enter second float: "))
sum_total = num1 + num2
print("Mathematical Sum:", sum_total)
```

```text
┌───────────────────────────┬─────────────────────────────────────────────────┐
│ Target Type               │ Conversion Function                             │
├───────────────────────────┼─────────────────────────────────────────────────┤
│ Integer                   │ `int(input("Enter whole number: "))`            │
│ Floating-Point            │ `float(input("Enter decimal number: "))`        │
│ Boolean (via comparison)  │ `input("Proceed? (y/n): ").strip().lower() == 'y'`│
└───────────────────────────┴─────────────────────────────────────────────────┘
```

### 3.3 Prompt Engineering and Formatting

Formatting prompts clearly reduces user error. Include formatting units, boundary hints, and trailing spaces for clean terminal aesthetics:

```python
# Poor prompt formatting (cursor directly touches prompt text):
# raw = input("Enter age:")

# Clean prompt formatting:
user_age = int(input("Enter your age in years (1-120): "))
```

### 3.4 Parsing Multi-Value Input

Multiple space-separated or delimiter-separated values can be collected in a single line using string splitting and mapping functions:

```python
# Example 1: Reading two strings separated by space
first_name, last_name = input("Enter first and last name: ").split()
print("First:", first_name)
print("Last:", last_name)

# Example 2: Reading multiple integers in one line using map()
dimensions = list(map(int, input("Enter width and height (e.g. 1920 1080): ").split()))
print("Parsed dimensions:", dimensions)
```

### 3.5 Input Sanitization and Basic Validation

Raw input may contain accidental leading/trailing whitespace or invalid characters. Applying basic string sanitization prevents downstream errors:

```python
raw_input_email = input("Enter user email: ")
sanitized_email = raw_input_email.strip().lower()

# Verification of numeric formatting before conversion
user_selection = input("Select menu option (1-5): ").strip()
if user_selection.isdigit():
    option = int(user_selection)
    print("Option selected:", option)
else:
    print("Invalid numeric selection.")
```

### 3.6 Practical Interactive CLI Implementations

Below is an interactive currency exchange rate converter:

```python
# currency_converter.py
print("=" * 40)
print("   EXCHANGE RATE CONVERSION UTILITY   ")
print("=" * 40)

usd_amount_str = input("Enter base amount in USD ($): ").strip()
rate_str = input("Enter USD to EUR conversion rate (e.g. 0.92): ").strip()

usd_amount = float(usd_amount_str)
rate = float(rate_str)
eur_amount = usd_amount * rate

print("-" * 40)
print(f"Base Amount: ${usd_amount:,.2f} USD")
print(f"Exchange Rate: {rate}")
print(f"Converted Amount: €{eur_amount:,.2f} EUR")
print("=" * 40)
```

### 3.7 Section Exercises & Solutions

#### Exercise 3.1: Circle Measurement Calculator
Write a script that prompts for the radius of a circle as a floating-point number. Calculate and display the circumference ($C = 2 \pi r$) and the area ($A = \pi r^2$) using $\pi = 3.14159265$. Format the output to four decimal places.

<details>
<summary><b>View Solution</b></summary>

```python
PI = 3.14159265

radius_input = input("Enter circle radius: ").strip()
radius = float(radius_input)

circumference = 2 * PI * radius
area = PI * (radius ** 2)

print(f"Circumference: {circumference:.4f}")
print(f"Area:          {area:.4f}")
```
</details>

---

## 4. Data Types

### 4.1 Numeric Types (`int`, `float`, `complex`)

Python features three built-in numeric representations:

```python
# 1. Integer (int): Arbitrary-precision whole numbers
item_count = 500
large_value = 1_000_000_000  # Underscores serve as visual digit separators

# Alternate base representations:
bin_val = 0b1010  # Binary (Decimal: 10)
oct_val = 0o12    # Octal (Decimal: 10)
hex_val = 0x0A    # Hexadecimal (Decimal: 10)

# 2. Floating-Point (float): IEEE 754 standard double-precision real numbers
temperature = 98.6
scientific_val = 1.25e-4  # 0.000125

# 3. Complex Number (complex): Real and imaginary parts
voltage = 3.0 + 4.5j
print("Real part:", voltage.real)
print("Imaginary part:", voltage.imag)
```

### 4.2 Boolean Type (`bool`)

The `bool` type is a subclass of `int` and contains exactly two constant instances: `True` (integer value 1) and `False` (integer value 0).

```python
is_authenticated = True
has_permission = False

print(type(is_authenticated))  # <class 'bool'>
print(int(True))               # 1
print(int(False))              # 0
```

### 4.3 The None Type (`NoneType`)

`None` is a singleton object representing the intentional absence of a value or a null pointer. Functions that do not explicitly return a value return `None` by default.

```python
database_handle = None

if database_handle is None:
    print("Database connection uninitialized.")
```

### 4.4 Type Inspection and Type Casting

Type inspection evaluates the class hierarchy of an object, while type casting explicitly converts an object between compatible types.

```python
sample_data = 100

# Type inspection
print(type(sample_data))                 # <class 'int'>
print(isinstance(sample_data, int))      # True
print(isinstance(sample_data, (int, str))) # True (checks tuple of types)

# Explicit Type Casting
cast_float = float(sample_data)          # 100.0
cast_str = str(sample_data)              # "100"
cast_bool = bool(sample_data)            # True
```

### 4.5 Text Sequence Type (`str`)

Strings (`str`) are immutable sequences of Unicode characters.

```python
single_quoted = 'String in single quotes'
double_quoted = "String in double quotes"
multi_line = """This is a
multi-line string literal."""
```

### 4.6 String Indexing and Slicing

Strings support 0-based indexing from the beginning and negative indexing from the end.

```text
 Index (Forward):   0   1   2   3   4   5
 Character:         P   y   t   h   o   n
 Index (Reverse):  -6  -5  -4  -3  -2  -1
```

```python
text = "Python"

# Indexing
print(text[0])     # 'P'
print(text[-1])    # 'n'

# Slicing: sequence[start:stop:step] (stop is non-inclusive)
print(text[0:4])   # 'Pyth'
print(text[:3])    # 'Pyt'
print(text[3:])    # 'hon'
print(text[::2])   # 'Pto' (every second character)
print(text[::-1])  # 'nohtyP' (reversed string)
```

### 4.7 String Immutability

String objects cannot be modified in-place after instantiation. Attempting item assignment raises a `TypeError`.

```python
label = "State"
# label[0] = "D"  # Raises TypeError: 'str' object does not support item assignment

# Correct modification creates a new string object:
new_label = "D" + label[1:]
print(new_label)  # "Dtate"
```

### 4.8 Built-in String Methods

String methods do not mutate the caller; they return newly generated string instances.

```python
message = "   Standard System Payload Data   "

# 1. Trimming whitespace
clean = message.strip()            # "Standard System Payload Data"

# 2. Case transformation
lower_case = clean.lower()         # "standard system payload data"
upper_case = clean.upper()         # "STANDARD SYSTEM PAYLOAD DATA"
title_case = clean.title()         # "Standard System Payload Data"

# 3. Search and validation
starts_with = clean.startswith("Std") # False
ends_with = clean.endswith("Data")   # True
pos_index = clean.find("System")      # 9 (returns -1 if absent)
occurrences = clean.count("a")        # 5

# 4. Replacement
replaced = clean.replace("Payload", "Diagnostic")
# "Standard System Diagnostic Data"

# 5. Splitting and Joining
tokens = clean.split(" ")          # ['Standard', 'System', 'Payload', 'Data']
joined_str = "-".join(tokens)      # "Standard-System-Payload-Data"
```

### 4.9 Formatted String Literals (f-strings)

Introduced in Python 3.6, f-strings provide concise inline interpolation and formatting specification.

```python
metric_name = "Latency"
duration_ms = 4.28764
requests_count = 15000

# Basic interpolation
print(f"Metric: {metric_name} | Value: {duration_ms}")

# Precision formatting (:.<N>f)
print(f"Rounded Duration: {duration_ms:.2f} ms")  # 4.29 ms

# Numeric digit grouping
print(f"Total Processed: {requests_count:,}")     # 15,000

# Padding and alignment
print(f"{metric_name:<15} : {duration_ms:>10.2f}")
```

### 4.10 Escape Sequences and Raw Strings

Backslashes introduce escape sequences representing non-printable or special characters:

| Escape Sequence | Representation |
| :---: | :--- |
| `\n` | Linefeed (Newline) |
| `\t` | Horizontal Tab |
| `\\` | Literal Backslash |
| `\'` | Literal Single Quote |
| `\"` | Literal Double Quote |

**Raw Strings (`r"..."`)** suppress escape interpretation, treating backslashes as literal characters:
```python
standard_path = "C:\\Windows\\System32\\drivers"
raw_path = r"C:\Windows\System32\drivers"
```

### 4.11 Section Exercises & Solutions

#### Exercise 4.1: URL Protocol and Domain Parser
Given the complete URL `target_url = "https://api.internal.service.io:8080/v1/status"`, extract:
1. The protocol (`"https"`)
2. The domain name with port (`"api.internal.service.io:8080"`)
3. The resource path (`"/v1/status"`)

<details>
<summary><b>View Solution</b></summary>

```python
target_url = "https://api.internal.service.io:8080/v1/status"

protocol, rest = target_url.split("://")
domain_with_port, path_part = rest.split("/", 1)
resource_path = "/" + path_part

print(f"Protocol: {protocol}")
print(f"Domain:   {domain_with_port}")
print(f"Path:     {resource_path}")
```
</details>

---

## 5. Operators

### 5.1 Arithmetic Operators

Arithmetic operators execute standard mathematical computations:

| Operator | Syntax | Description | Example (`a = 15, b = 4`) | Result |
| :---: | :---: | :--- | :---: | :---: |
| `+` | `a + b` | Addition | `15 + 4` | `19` |
| `-` | `a - b` | Subtraction | `15 - 4` | `11` |
| `*` | `a * b` | Multiplication | `15 * 4` | `60` |
| `/` | `a / b` | True Division (Always returns `float`) | `15 / 4` | `3.75` |
| `//` | `a // b`| Floor Division (Rounds down to nearest integer) | `15 // 4` | `3` |
| `%` | `a % b` | Modulus (Remainder after division) | `15 % 4` | `3` |
| `**` | `a ** b`| Exponentiation ($a^b$) | `2 ** 3` | `8` |

### 5.2 Assignment and Augmented Assignment Operators

Assignment operators bind or mutate variable references:

```python
total = 100
total += 25   # Equivalent to: total = total + 25   -> 125
total -= 10   # Equivalent to: total = total - 10   -> 115
total *= 2    # Equivalent to: total = total * 2    -> 230
total /= 5    # Equivalent to: total = total / 5    -> 46.0
total //= 4   # Equivalent to: total = total // 4   -> 11.0
total %= 3    # Equivalent to: total = total % 3    -> 2.0
total **= 3   # Equivalent to: total = total ** 3   -> 8.0
```

### 5.3 Comparison (Relational) Operators

Comparison operators evaluate relational conditions, returning boolean values (`True` or `False`):

| Operator | Description | Example (`x = 10, y = 20`) | Result |
| :---: | :--- | :---: | :---: |
| `==` | Equal to | `x == y` | `False` |
| `!=` | Not equal to | `x != y` | `True` |
| `>` | Strictly greater than | `x > y` | `False` |
| `<` | Strictly less than | `x < y` | `True` |
| `>=` | Greater than or equal to | `x >= 10` | `True` |
| `<=` | Less than or equal to | `y <= 20` | `True` |

> Python supports **chained comparisons**: `10 <= x < 50` is evaluated as `(10 <= x) and (x < 50)`.

### 5.4 Logical Operators and Short-Circuit Evaluation

Logical operators combine boolean conditions:

| Operator | Evaluation Behavior |
| :---: | :--- |
| `and` | Returns `True` only if **both** operands evaluate to true. |
| `or` | Returns `True` if **at least one** operand evaluates to true. |
| `not` | Unary operator that inverts the truth value of the operand. |

#### Short-Circuit Mechanics
- In an `and` operation, if the left operand is false, the expression immediately evaluates to the left operand without executing the right operand.
- In an `or` operation, if the left operand is true, the expression immediately evaluates to the left operand without executing the right operand.

```python
def check_connection():
    print("Executing check_connection()...")
    return False

# The function is never invoked because False on the left short-circuits the 'and' condition:
result = False and check_connection()
```

### 5.5 Bitwise Operators

Bitwise operators manipulate integers at the binary bit level:

```python
a = 0b1100  # 12
b = 0b1010  # 10

print(bin(a & b))   # Bitwise AND: 0b1000 (8)
print(bin(a | b))   # Bitwise OR:  0b1110 (14)
print(bin(a ^ b))   # Bitwise XOR: 0b0110 (6)
print(bin(~a))      # Bitwise NOT: -13 (Two's complement)
print(bin(a << 2))  # Left Shift:  0b110000 (48)
print(bin(a >> 2))  # Right Shift: 0b0011 (3)
```

### 5.6 Identity Operators (`is`, `is not`)

Identity operators evaluate whether two variables reference the **exact same memory address** (`id(a) == id(b)`), in contrast to value equality (`==`).

```python
list_1 = [1, 2, 3]
list_2 = [1, 2, 3]
list_3 = list_1

print(list_1 == list_2)  # True  (Identical contents)
print(list_1 is list_2)  # False (Distinct objects in memory)
print(list_1 is list_3)  # True  (Identical object reference)

# Idiomatic check for None:
value = None
print(value is None)     # True
```

### 5.7 Membership Operators (`in`, `not in`)

Membership operators test for presence within sequences, mappings, or sets:

```python
registered_users = ["admin", "operator", "auditor"]
print("admin" in registered_users)       # True
print("guest" not in registered_users)   # True

config_keys = {"host": "127.0.0.1", "port": 5432}
print("host" in config_keys)             # True (Checks dictionary keys)
print("127.0.0.1" in config_keys)        # False (Does not check values by default)
```

### 5.8 Operator Precedence and Associativity

Expressions are resolved in order of precedence (highest to lowest):

```text
┌───────────────────────────────────────────────────────────┬──────────────┐
│ Operators                                                 │ Associativity│
├───────────────────────────────────────────────────────────┼──────────────┤
│ `()` (Parentheses / Grouping)                             │ Left-to-Right│
│ `**` (Exponentiation)                                     │ Right-to-Left│
│ `+x`, `-x`, `~x` (Unary positive, negative, bitwise NOT)  │ Right-to-Left│
│ `*`, `/`, `//`, `%` (Multiplication, Division, Modulo)    │ Left-to-Right│
│ `+`, `-` (Addition, Subtraction)                          │ Left-to-Right│
│ `<<`, `>>` (Bitwise shifts)                               │ Left-to-Right│
│ `&` (Bitwise AND)                                         │ Left-to-Right│
│ `^` (Bitwise XOR)                                         │ Left-to-Right│
│ `|` (Bitwise OR)                                          │ Left-to-Right│
│ `==`, `!=`, `<`, `<=`, `>`, `>=`, `is`, `is not`, `in`    │ Left-to-Right│
│ `not` (Logical NOT)                                       │ Right-to-Left│
│ `and` (Logical AND)                                       │ Left-to-Right│
│ `or` (Logical OR)                                         │ Left-to-Right│
│ `=`, `+=`, `-=`, `*=`, etc. (Assignments)                 │ Right-to-Left│
└───────────────────────────────────────────────────────────┴──────────────┘
```

### 5.9 Section Exercises & Solutions

#### Exercise 5.1: Network Subnet Matcher
Write an expression that evaluates to `True` if an IP address string belongs to a local range:
1. `ip_address` starts with `"192.168."` OR `"10."`
2. `port` is equal to 80, 443, or 8080
3. `is_blacklisted` is `False`

<details>
<summary><b>View Solution</b></summary>

```python
ip_address = "192.168.1.45"
port = 443
is_blacklisted = False

is_allowed = (
    (ip_address.startswith("192.168.") or ip_address.startswith("10."))
    and (port in (80, 443, 8080))
    and (not is_blacklisted)
)

print("Connection permitted:", is_allowed)
```
</details>

---

## 6. Flow Control

### 6.1 Conditional Statements (`if`, `elif`, `else`)

Conditional branching directs execution along discrete pathways based on truth evaluations:

```python
http_status = 404

if http_status == 200:
    print("OK: Request succeeded.")
elif http_status == 301:
    print("Moved Permanently: Resource redirected.")
elif http_status == 404:
    print("Not Found: Resource does not exist.")
elif http_status == 500:
    print("Internal Server Error: Execution failure on remote host.")
else:
    print(f"Unknown status code: {http_status}")
```

### 6.2 Nested Conditionals and Multi-Branch Logic

Conditionals can be nested within existing blocks to model hierarchical decisions:

```python
user_authenticated = True
access_level = "admin"
mfa_verified = True

if user_authenticated:
    if access_level == "admin":
        if mfa_verified:
            print("Access granted: Full Administrative Privileges.")
        else:
            print("Access denied: Multi-Factor Authentication required.")
    else:
        print("Access granted: Standard User Privileges.")
else:
    print("Access denied: Unauthenticated session.")
```

### 6.3 Truthy and Falsy Evaluation Rules

When evaluated in a boolean context, all Python objects inherently cast to either `True` or `False`.

```text
┌───────────────────────────────────────┬───────────────────────────────────────┐
│             Falsy Values              │             Truthy Values             │
├───────────────────────────────────────┼───────────────────────────────────────┤
│ • Constant `False`                    │ • Constant `True`                     │
│ • Singleton `None`                    │ • Non-zero numeric values (`1`, `-5`) │
│ • Numeric zeros (`0`, `0.0`, `0j`)    │ • Non-empty strings (`"Data"`, `" "`) │
│ • Empty sequences (`""`, `[]`, `()`)  │ • Non-empty collections               │
│ • Empty mappings (`{}`, `set()`)      │   (`[0]`, `{"status": False}`)        │
└───────────────────────────────────────┴───────────────────────────────────────┘
```

```python
# Idiomatic verification using truthiness:
active_connections = []

if not active_connections:
    print("Connection pool is depleted.")
```

### 6.4 Conditional Expressions (Ternary Operator)

The ternary operator enables single-line conditional assignments using the syntax:
`value_if_true if condition else value_if_false`

```python
latency_ms = 45
system_health = "Optimal" if latency_ms < 50 else "Degraded"
print("Status:", system_health)
```

### 6.5 Structural Pattern Matching (`match...case`)

Introduced in Python 3.10, structural pattern matching evaluates an expression against discrete structural patterns:

```python
def parse_command(command_tuple):
    match command_tuple:
        case ("GET", resource):
            print(f"Fetching resource: {resource}")
        case ("POST", resource, payload):
            print(f"Submitting payload to {resource}: {payload}")
        case ("DELETE", resource) if resource != "/root":
            print(f"Deleting resource: {resource}")
        case ("DELETE", "/root"):
            print("Action Prohibited: Root resource cannot be deleted.")
        case _:
            print("Unrecognized command structure.")

parse_command(("GET", "/users/all"))
parse_command(("POST", "/users", {"id": 101}))
parse_command(("DELETE", "/root"))
```

### 6.6 Guard Clauses and Branch Cleanliness

Deeply nested logic increases cognitive complexity. Guard clauses handle error conditions and edge cases early, leaving happy-path logic unindented:

```python
# ❌ Anti-pattern: Deep nesting
def process_transaction(user, account, amount):
    if user is not None:
        if account.is_active:
            if account.balance >= amount:
                account.balance -= amount
                return True
            else:
                return False
        else:
            return False
    else:
        return False

# ✅ Best Practice: Guard Clauses
def process_transaction_clean(user, account, amount):
    if user is None:
        return False
    if not account.is_active:
        return False
    if account.balance < amount:
        return False

    account.balance -= amount
    return True
```

### 6.7 Section Exercises & Solutions

#### Exercise 6.1: Bandwidth Throttling Classifier
Write a classifier that determines rate limits based on user tier and current consumption:
- If `tier == "free"`, max bandwidth is 50 Mbps.
- If `tier == "pro"`, max bandwidth is 200 Mbps.
- If `tier == "enterprise"`, max bandwidth is 1000 Mbps.
- If `current_usage > max_bandwidth`, output `"Throttling Active"`, otherwise output `"Bandwidth Compliant"`.

<details>
<summary><b>View Solution</b></summary>

```python
tier = "pro"
current_usage = 240

match tier:
    case "free":
        max_bandwidth = 50
    case "pro":
        max_bandwidth = 200
    case "enterprise":
        max_bandwidth = 1000
    case _:
        max_bandwidth = 0

status = "Throttling Active" if current_usage > max_bandwidth else "Bandwidth Compliant"
print(f"Tier: {tier} | Usage: {current_usage}/{max_bandwidth} Mbps | Result: {status}")
```
</details>

---

## 7. Loops

### 7.1 Definite vs. Indefinite Iteration

- **Definite Iteration (`for` loop):** Executes a block of statements a predetermined number of times, or across each item in a collection.
- **Indefinite Iteration (`while` loop):** Executes continuously as long as a specified condition remains `True`.

### 7.2 The `while` Loop and Infinite Loop Prevention

A `while` loop checks its test condition before every iteration:

```python
counter = 1
while counter <= 5:
    print(f"Loop iteration: {counter}")
    counter += 1  # State mutation to guarantee loop termination

print("Execution proceeded past loop.")
```

> **Infinite Loop Mitigation:** Ensure the loop state variable is guaranteed to reach the termination boundary. In CLI environments, a stuck loop can be halted with `Ctrl+C`.

### 7.3 The `for` Loop and the `range()` Function

The `for` loop implements the Python Iteration Protocol across iterable objects:

```python
# Iterating over sequence items
for character in "Python":
    print(character, end=" ")
print()
```

#### Anatomy of `range()`
The `range(start, stop, step)` built-in returns an immutable arithmetic sequence:
- `start` (optional, default: 0): Inclusive initial integer.
- `stop` (required): Non-inclusive terminal boundary.
- `step` (optional, default: 1): Increment step size.

```python
# Range from 0 to 4
for i in range(5):
    print(i, end=" ")  # 0 1 2 3 4
print()

# Range from 10 to 50 with step 10
for i in range(10, 51, 10):
    print(i, end=" ")  # 10 20 30 40 50
print()

# Reverse range from 5 down to 1
for i in range(5, 0, -1):
    print(i, end=" ")  # 5 4 3 2 1
print()
```

### 7.4 Loop Control Statements (`break`, `continue`, `pass`)

- `break`: Immediately terminates execution of the innermost enclosing loop.
- `continue`: Skips the remainder of the current iteration and jumps to the next cycle.
- `pass`: A null operation used as a syntactic placeholder.

```python
for number in range(1, 10):
    if number == 3:
        # Skip processing 3
        continue
    if number == 7:
        # Terminate iteration upon reaching 7
        break
    print("Processed:", number)
```

### 7.5 The Loop `else` Clause

Python loops support an optional `else` block. The `else` block executes **only if the loop terminates naturally without hitting a `break` statement**.

```python
search_target = 42
data_stream = [10, 23, 35, 78, 99]

for item in data_stream:
    if item == search_target:
        print(f"Found target {search_target} in data stream.")
        break
else:
    print(f"Target {search_target} was not present in the data stream.")
```

### 7.6 Nested Loops and Coordinate Grids

Placing one loop inside another produces nested iterations, commonly used for multidimensional matrices or Cartesian products:

```python
# 3x3 Matrix coordinate generation
for row in range(1, 4):
    for col in range(1, 4):
        print(f"[{row},{col}]", end=" ")
    print()  # Newline at row boundary
```

### 7.7 Iteration Helpers (`enumerate()`, `zip()`, `reversed()`, `sorted()`)

#### `enumerate(iterable, start=0)`
Generates index-value pairs during iteration:
```python
services = ["Auth", "Payments", "Notifications"]
for index, service in enumerate(services, start=1):
    print(f"{index}. {service}")
```

#### `zip(*iterables)`
Iterates over multiple sequences concurrently:
```python
keys = ["host", "port", "timeout"]
values = ["127.0.0.1", 8080, 30]

for key, value in zip(keys, values):
    print(f"{key} => {value}")
```

#### `reversed()` and `sorted()`
```python
raw_scores = [88, 95, 72, 100]
for score in sorted(raw_scores):
    print("Ascending score:", score)
```

### 7.8 Section Exercises & Solutions

#### Exercise 7.1: Prime Number Range Scanner
Write a script using nested loops to find and print all prime numbers between 2 and 50. Use a `for...else` construct.

<details>
<summary><b>View Solution</b></summary>

```python
primes = []

for num in range(2, 51):
    for divisor in range(2, int(num ** 0.5) + 1):
        if num % divisor == 0:
            break
    else:
        primes.append(num)

print("Prime numbers (2-50):", primes)
```
</details>

---

## 8. Data Structures

### 8.1 Core Collection Comparison

Python provides four fundamental built-in collection types:

```text
┌────────────┬─────────────┬───────────┬───────────┬──────────────┬───────────────────────────────┐
│ Collection │ Syntax      │ Ordered?  │ Mutable?  │ Duplicates?  │ Typical Use Case              │
├────────────┼─────────────┼───────────┼───────────┼──────────────┼───────────────────────────────┤
│ **List**   │ `[1, 2, 3]` │ Yes       │ Yes       │ Yes          │ Sequential collections, queues│
│ **Tuple**  │ `(1, 2, 3)` │ Yes       │ No        │ Yes          │ Fixed records, dict keys      │
│ **Set**    │ `{1, 2, 3}` │ No        │ Yes       │ No (Unique)  │ Membership tests, set math    │
│ **Dict**   │ `{"k": "v"}`│ Yes (3.7+)│ Yes       │ Keys: Unique │ Key-value lookup tables, JSON │
└────────────┴─────────────┴───────────┴───────────┴──────────────┴───────────────────────────────┘
```

### 8.2 Lists (Ordered, Mutable Sequences)

Lists store an ordered sequence of heterogeneous objects.

```python
# Instantiation
buffer = [10, "ready", 4.5, True]

# Modification and indexing
buffer[1] = "active"          # In-place item replacement
buffer.append("new_element")  # Appends to end: O(1)
buffer.insert(0, "header")    # Inserts at index: O(N)
buffer.extend([100, 200])     # Appends sequence to end

# Removal
removed_item = buffer.pop()   # Removes and returns last element: O(1)
buffer.remove("active")       # Removes first matching value: O(N)
del buffer[0]                 # Removes item at index 0

# Utility methods
numeric_list = [45, 12, 89, 3, 27]
numeric_list.sort()           # Sorts list in-place (Timsort: O(N log N))
numeric_list.reverse()        # Reverses list in-place
print("Sorted & Reversed:", numeric_list)
```

### 8.3 Tuples (Ordered, Immutable Sequences)

Tuples protect data integrity by preventing modification after instantiation.

```python
# Creation (Single-element tuples require a trailing comma)
point_3d = (10, 20, 30)
single_item = ("data",)

# Tuple Unpacking
x, y, z = point_3d
print(f"X: {x}, Y: {y}, Z: {z}")

# Extended Unpacking with Asterisk (*)
first, *middle, last = [1, 2, 3, 4, 5, 6]
print("First:", first)   # 1
print("Middle:", middle) # [2, 3, 4, 5]
print("Last:", last)     # 6
```

### 8.4 Sets (Unordered, Unique Hashable Collections)

Sets store unique, hashable objects and provide fast membership testing ($O(1)$ average complexity).

```python
# Creation (Empty set must use set(), as {} initializes a dictionary)
roles = {"admin", "editor", "viewer", "editor"}
print(roles)  # {'admin', 'editor', 'viewer'} (Duplicates dropped)

# Mutation
roles.add("auditor")
roles.discard("viewer")  # Safely removes item without raising KeyError if absent

# Set Mathematical Operations
set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}

print(set_a | set_b)  # Union: {1, 2, 3, 4, 5, 6}
print(set_a & set_b)  # Intersection: {3, 4}
print(set_a - set_b)  # Difference: {1, 2}
print(set_a ^ set_b)  # Symmetric Difference: {1, 2, 5, 6}
```

### 8.5 Dictionaries (Key-Value Hash Maps)

Dictionaries map unique, hashable keys to arbitrary object values.

```python
server_config = {
    "host": "localhost",
    "port": 8000,
    "ssl_enabled": False,
    "allowed_hosts": ["127.0.0.1", "::1"]
}

# Accessing Values
print(server_config["host"])                         # "localhost"
print(server_config.get("timeout", 30))              # 30 (Default fallback if key missing)

# Insertion and Mutation
server_config["port"] = 8443                         # Update existing key
server_config["max_workers"] = 4                     # Insert new key-value pair

# Dictionary Merging (Python 3.9+ Union Operator)
override_config = {"port": 9000, "debug": True}
merged_config = server_config | override_config

# Dictionary Iteration
for key, value in merged_config.items():
    print(f"{key:<15} : {value}")
```

### 8.6 Comprehensions (List, Set, Dict, Generator Expressions)

Comprehensions construct collections declaratively:

```python
# 1. List Comprehension: [expression for item in iterable if condition]
even_squares = [x ** 2 for x in range(10) if x % 2 == 0]
# [0, 4, 16, 36, 64]

# 2. Set Comprehension
unique_lengths = {len(word) for word in ["apple", "banana", "pear", "apple"]}
# {4, 5, 6}

# 3. Dict Comprehension
word_lengths = {word: len(word) for word in ["python", "c", "rust"]}
# {'python': 6, 'c': 1, 'rust': 4}

# 4. Generator Expression (Lazy evaluation, memory-efficient)
gen_squares = (x ** 2 for x in range(1000000))
print(next(gen_squares))  # 0
print(next(gen_squares))  # 1
```

### 8.7 Specialized Collections (`collections` Module)

The standard `collections` module provides enhanced data structures:

```python
from collections import deque, Counter, defaultdict

# 1. deque: Fast O(1) appends and pops from both ends
task_queue = deque(["task_1", "task_2"])
task_queue.appendleft("urgent_task")
task_queue.pop()

# 2. Counter: Frequency multiset
inventory = Counter(["apple", "banana", "apple", "orange", "apple"])
print(inventory["apple"])           # 3
print(inventory.most_common(1))     # [('apple', 3)]

# 3. defaultdict: Automatic initialization for missing keys
grouped_data = defaultdict(list)
grouped_data["engineers"].append("Alice")
grouped_data["designers"].append("Bob")
```

### 8.8 Algorithmic Complexity (Big-O) Overview

| Operation | List (`list`) | Set (`set`) | Dictionary (`dict`) |
| :--- | :--- | :--- | :--- |
| **Index Access** | $O(1)$ | N/A | N/A |
| **Key Lookup** | N/A | $O(1)$ avg | $O(1)$ avg |
| **Membership (`x in s`)** | $O(N)$ | $O(1)$ avg | $O(1)$ avg (keys) |
| **Append / Insert End** | $O(1)$ | $O(1)$ avg | $O(1)$ avg |
| **Insert Arbitrary** | $O(N)$ | N/A | N/A |
| **Delete** | $O(N)$ | $O(1)$ avg | $O(1)$ avg |

### 8.9 Section Exercises & Solutions

#### Exercise 8.1: Inverted Index Builder
Given a dictionary mapping documents to their word lists:
`docs = {"doc1": ["python", "code", "guide"], "doc2": ["python", "reference"], "doc3": ["code", "style"]}`
Build an inverted index mapping each unique word to a set of document IDs containing it.

<details>
<summary><b>View Solution</b></summary>

```python
docs = {
    "doc1": ["python", "code", "guide"],
    "doc2": ["python", "reference"],
    "doc3": ["code", "style"]
}

inverted_index = {}

for doc_id, words in docs.items():
    for word in words:
        if word not in inverted_index:
            inverted_index[word] = set()
        inverted_index[word].add(doc_id)

for word, doc_set in sorted(inverted_index.items()):
    print(f"'{word}': {doc_set}")
```
</details>

---

## 9. Functions

### 9.1 Modular Architecture and Reusability

Functions are named blocks of reusable code designed to perform a distinct, well-defined task. They promote maintainability, modularity, and adherence to the **DRY (Don't Repeat Yourself)** principle.

### 9.2 Function Definition and Invocation

Functions are declared with the `def` keyword, followed by the identifier, parameter signature, and colon.

```python
# Function Definition
def calculate_throughput(requests: int, time_seconds: float) -> float:
    if time_seconds <= 0:
        return 0.0
    return requests / time_seconds

# Function Invocation
rps = calculate_throughput(1200, 30.0)
print(f"Throughput: {rps:.2f} Req/Sec")
```

### 9.3 Parameters vs. Arguments

- **Parameter:** The variable declared in the function definition header.
- **Argument:** The concrete value passed into the function during invocation.

### 9.4 Positional, Keyword, and Default Arguments

```python
def configure_server(host, port=8080, use_tls=True):
    return f"Configured {host}:{port} (TLS: {use_tls})"

# Positional invocation
print(configure_server("10.0.0.1"))

# Keyword invocation (independent of parameter order)
print(configure_server(use_tls=False, host="192.168.1.1", port=9000))
```

> [!CAUTION]
> **Mutable Default Argument Pitfall:** Default parameters are evaluated once when the function is defined, not on each invocation. Never use mutable objects (`[]`, `{}`) as default parameters. Use `None` as the sentinel default value instead.

```python
# ❌ Anti-Pattern: Shared mutable list across invocations
# def append_task(task, task_list=[]):
#     task_list.append(task)
#     return task_list

# ✅ Best Practice:
def append_task(task, task_list=None):
    if task_list is None:
        task_list = []
    task_list.append(task)
    return task_list
```

### 9.5 Variable-Length Arguments (`*args`, `**kwargs`)

- `*args`: Collects excess positional arguments into a **tuple**.
- `**kwargs`: Collects excess keyword arguments into a **dictionary**.

```python
def build_query(table_name, *columns, **filters):
    cols_clause = ", ".join(columns) if columns else "*"
    query = f"SELECT {cols_clause} FROM {table_name}"
    
    if filters:
        filter_clauses = [f"{k} = '{v}'" for k, v in filters.items()]
        query += " WHERE " + " AND ".join(filter_clauses)
        
    return query

sql = build_query("users", "id", "username", "email", role="admin", active="True")
print(sql)
# SELECT id, username, email FROM users WHERE role = 'admin' AND active = 'True'
```

### 9.6 Positional-Only (`/`) and Keyword-Only (`*`) Parameters

- Parameters preceding `/` must be supplied positionally.
- Parameters following `*` must be supplied as keyword arguments.

```python
def standard_api(pos_only, /, standard_param, *, kw_only):
    print(pos_only, standard_param, kw_only)

# Valid invocation:
standard_api(1, 2, kw_only=3)
standard_api(1, standard_param=2, kw_only=3)
```

### 9.7 Return Values and Multiple Return Unpacking

Functions terminate immediately upon encountering a `return` statement. Multiple values returned in a single statement are packed into a tuple:

```python
def get_dataset_statistics(numbers):
    if not numbers:
        return 0, 0.0, 0
    return min(numbers), sum(numbers) / len(numbers), max(numbers)

min_val, avg_val, max_val = get_dataset_statistics([12, 45, 67, 89, 23])
print(f"Min: {min_val}, Avg: {avg_val:.2f}, Max: {max_val}")
```

### 9.8 Variable Scope and Namespace (LEGB Rule)

Python resolves variable names using the **LEGB hierarchy**:

```text
┌────────────────────────────────────────────────────────┐
│ Local (L): Variables declared within current function  │
├────────────────────────────────────────────────────────┤
│ Enclosing (E): Variables in outer enclosing functions  │
├────────────────────────────────────────────────────────┤
│ Global (G): Variables defined at module root level     │
├────────────────────────────────────────────────────────┤
│ Built-in (B): Predefined names (e.g., print, range)    │
└────────────────────────────────────────────────────────┘
```

```python
global_config_name = "PRODUCTION"

def outer_service():
    service_id = "SVC_01"

    def inner_worker():
        nonlocal service_id  # Modifies variable in enclosing scope
        service_id = "SVC_01_MODIFIED"
        print("Inside worker, global is:", global_config_name)

    inner_worker()
    print("Outer service_id:", service_id)

outer_service()
```

### 9.9 First-Class Functions and Higher-Order Functions

In Python, functions are **first-class objects**: they can be assigned to variables, passed as arguments, and returned from other functions.

```python
def format_json(data):
    return f'{{"data": "{data}"}}'

def format_xml(data):
    return f'<data>{data}</data>'

def emit_payload(formatter_fn, raw_content):
    # Function passed as parameter
    return formatter_fn(raw_content)

print(emit_payload(format_json, "Payload 101"))
print(emit_payload(format_xml, "Payload 101"))
```

### 9.10 Closures and Decorators

A **closure** occurs when an inner function retains access to variables from its enclosing lexical scope even after the outer function has finished executing.

A **decorator** is a higher-order function that dynamically wraps and extends the behavior of another function without altering its source code.

```python
import time
from functools import wraps

def benchmark_timer(target_function):
    @wraps(target_function)
    def wrapper(*args, **kwargs):
        start_time = time.perf_counter()
        result = target_function(*args, **kwargs)
        end_time = time.perf_counter()
        print(f"[BENCHMARK] '{target_function.__name__}' executed in {end_time - start_time:.6f}s")
        return result
    return wrapper

@benchmark_timer
def compute_heavy_task(n):
    return sum(i ** 2 for i in range(n))

compute_heavy_task(100000)
```

### 9.11 Docstrings and Type Annotations

Documenting code with type hints and docstrings (PEP 257) enhances code maintainability and enables automated static analysis:

```python
def calculate_roi(investment: float, revenue: float) -> float:
    """
    Calculate Return on Investment (ROI) percentage.

    Parameters:
        investment (float): Total initial capital invested.
        revenue (float): Total gross revenue returned.

    Returns:
        float: ROI expressed as a percentage value.

    Raises:
        ValueError: If investment is less than or equal to zero.
    """
    if investment <= 0:
        raise ValueError("Investment must be strictly positive.")
    return ((revenue - investment) / investment) * 100
```

### 9.12 Section Exercises & Solutions

#### Exercise 9.1: Generic Retry Decorator
Create a function decorator `@retry(max_attempts=3)` that re-executes the decorated function up to `max_attempts` times if an exception is raised before allowing the exception to propagate.

<details>
<summary><b>View Solution</b></summary>

```python
from functools import wraps

def retry(max_attempts=3):
    def decorator(func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            attempts = 0
            while attempts < max_attempts:
                try:
                    return func(*args, **kwargs)
                except Exception as e:
                    attempts += 1
                    print(f"Attempt {attempts} failed with: {e}")
                    if attempts >= max_attempts:
                        raise e
        return wrapper
    return decorator

# Verification test
call_count = 0

@retry(max_attempts=3)
def unstable_network_call():
    global call_count
    call_count += 1
    if call_count < 3:
        raise ConnectionResetError("Network drop")
    return "Data Stream Online"

print("Result:", unstable_network_call())
```
</details>

---

## 10. Lambda Functions

### 10.1 Concept and Syntax of Anonymous Functions

A **lambda function** is a small, inline, anonymous function evaluated at runtime.
Syntax: `lambda parameter1, parameter2, ...: expression`

```python
# Simple lambda definition
square = lambda x: x ** 2
print(square(6))  # 36

# Multi-parameter lambda
compute_hypotenuse = lambda a, b: (a**2 + b**2) ** 0.5
print(compute_hypotenuse(3, 4))  # 5.0
```

### 10.2 Comparison: `def` Statements vs. `lambda` Expressions

```text
┌───────────────────────────────────────┬───────────────────────────────────────┐
│ Named Function (`def`)                │ Anonymous Lambda (`lambda`)          │
├───────────────────────────────────────┼───────────────────────────────────────┤
│ • Declared with formal identifier     │ • Anonymous (inline expression)       │
│ • Can contain statements, loops,      │ • Restricted strictly to a single     │
│   type annotations, and docstrings    │   expression with implicit return     │
│ • Reusable throughout codebase        │ • Typically used ephemerally as       │
│ • Easier to read in stack traces      │   arguments to higher-order functions │
└───────────────────────────────────────┴───────────────────────────────────────┘
```

### 10.3 Functional Operations (`map()`, `filter()`, `reduce()`)

#### `map(func, iterable)`
Applies a function to all elements in an iterable:
```python
temperatures_c = [0.0, 20.0, 37.0, 100.0]
temperatures_f = list(map(lambda c: (c * 9/5) + 32, temperatures_c))
print("Fahrenheit:", temperatures_f)
# [32.0, 68.0, 98.6, 212.0]
```

#### `filter(func, iterable)`
Extracts elements where the predicate function returns `True`:
```python
system_logs = ["INFO: Boot", "ERROR: DiskFull", "WARNING: Memory", "ERROR: Timeout"]
errors = list(filter(lambda log: log.startswith("ERROR"), system_logs))
print("Filtered Errors:", errors)
# ['ERROR: DiskFull', 'ERROR: Timeout']
```

#### `functools.reduce(func, iterable)`
Applies a rolling two-argument function across a sequence to reduce it to a single cumulative value:
```python
from functools import reduce
numbers = [1, 2, 3, 4, 5]
product = reduce(lambda acc, val: acc * val, numbers)
print("Product:", product)  # 120
```

### 10.4 Custom Sorting and Key Functions

Lambdas are extensively used as extraction `key` arguments for `sorted()`, `min()`, and `max()`:

```python
employees = [
    {"name": "Alice", "department": "Engineering", "salary": 95000},
    {"name": "Bob", "department": "Marketing", "salary": 65000},
    {"name": "Charlie", "department": "Engineering", "salary": 110000},
]

# 1. Sort employees by salary descending
sorted_by_salary = sorted(employees, key=lambda emp: emp["salary"], reverse=True)
print("Highest earner:", sorted_by_salary[0]["name"])

# 2. Sort strings case-insensitively and by length
words = ["Banana", "apple", "FIG", "cherry"]
words.sort(key=lambda s: (len(s), s.lower()))
print("Sorted words:", words)
```

### 10.5 Appropriate Use Cases and Anti-Patterns

- **Appropriate:** Inline key extractors in `sorted()`, `.sort()`, `min()`, `max()`, and lightweight event handlers.
- **Anti-Pattern:** Assigning lambdas to variables (PEP 8 recommends using `def` instead for named functions) or writing convoluted multi-branch lambdas.

```python
# ❌ Poor Practice: Assigning lambda to variable name
# is_even = lambda x: x % 2 == 0

# ✅ Preferred:
def is_even(x: int) -> bool:
    return x % 2 == 0
```

### 10.6 Section Exercises & Solutions

#### Exercise 10.1: Multi-Attribute Record Sorter
Given a list of transaction tuples `(transaction_id, customer_id, amount, status)`:
`transactions = [(101, 12, 450.0, "SETTLED"), (102, 18, 120.0, "PENDING"), (103, 12, 980.0, "SETTLED"), (104, 15, 310.0, "SETTLED")]`
Filter the list to include only `"SETTLED"` transactions, then sort the remaining records in descending order of `amount` using lambda functions.

<details>
<summary><b>View Solution</b></summary>

```python
transactions = [
    (101, 12, 450.0, "SETTLED"),
    (102, 18, 120.0, "PENDING"),
    (103, 12, 980.0, "SETTLED"),
    (104, 15, 310.0, "SETTLED")
]

# 1. Filter settled
settled = list(filter(lambda tx: tx[3] == "SETTLED", transactions))

# 2. Sort by amount descending
settled_sorted = sorted(settled, key=lambda tx: tx[2], reverse=True)

for tx in settled_sorted:
    print(f"TX {tx[0]} | Customer: {tx[1]} | Amount: ${tx[2]:.2f}")
```
</details>

---

## 11. File Handling

### 11.1 File Paths and Cross-Platform Operations (`pathlib`)

The built-in `pathlib` module provides an object-oriented, cross-platform interface for file system paths:

```python
from pathlib import Path

# Constructing paths cross-platform (handles / vs \ automatically)
base_dir = Path.cwd()
target_file = base_dir / "logs" / "application.log"

print("Absolute Path:", target_file.resolve())
print("File Exists:", target_file.exists())
print("Parent Directory:", target_file.parent)
print("File Suffix:", target_file.suffix)
```

### 11.2 File Open Modes

The built-in `open(file, mode='r', encoding=None)` function supports the following access modes:

| Mode | Name | Description |
| :---: | :--- | :--- |
| `'r'` | Read (Default) | Opens file for reading; raises `FileNotFoundError` if missing. |
| `'w'` | Write | Overwrites file completely or creates a new file. |
| `'a'` | Append | Writes new data at the end of the file; creates file if missing. |
| `'x'` | Exclusive Creation | Creates new file; raises `FileExistsError` if file exists. |
| `'b'` | Binary Mode | Reads/writes raw bytes (e.g., `'rb'`, `'wb'`) instead of text strings. |
| `'+'` | Read/Write Update | Allows simultaneous reading and writing (e.g., `'r+'`, `'w+'`). |

### 11.3 Context Managers and the `with` Statement

Using a `with` statement ensures the file handle is automatically and deterministically closed upon block exit, preventing resource leaks even if runtime exceptions occur:

```python
# Idiomatic File I/O
with open("system_config.txt", "w", encoding="utf-8") as file:
    file.write("MODE=PRODUCTION\n")
    file.write("LOG_LEVEL=INFO\n")
# File handle is safely closed here automatically
```

### 11.4 Reading Operations

```python
# 1. Read entire file into a single string (Caution on large files)
with open("system_config.txt", "r", encoding="utf-8") as file:
    full_content = file.read()

# 2. Read all lines into a list of strings
with open("system_config.txt", "r", encoding="utf-8") as file:
    lines_list = file.readlines()

# 3. Stream line-by-line (Memory-efficient: O(1) memory overhead)
with open("system_config.txt", "r", encoding="utf-8") as file:
    for line_num, line in enumerate(file, start=1):
        print(f"Line {line_num}: {line.strip()}")
```

### 11.5 Writing and Appending Operations

```python
records = ["Node_01: ONLINE", "Node_02: STANDBY", "Node_03: OFFLINE"]

# Writing multiple lines
with open("cluster_status.txt", "w", encoding="utf-8") as file:
    for record in records:
        file.write(record + "\n")

# Appending a new record
with open("cluster_status.txt", "a", encoding="utf-8") as file:
    file.write("Node_04: PROVISIONING\n")
```

### 11.6 File Cursor Management (`tell()`, `seek()`)

The file pointer tracks the current byte position within an open stream:
- `file.tell()`: Returns current integer byte position.
- `file.seek(offset, whence)`: Repositions the cursor (`whence`: 0=start, 1=current, 2=end).

```python
with open("sample_stream.txt", "w+", encoding="utf-8") as file:
    file.write("ABCDEFGHIJ")
    
    print("Cursor position after write:", file.tell())  # 10
    
    # Rewind cursor to start
    file.seek(0)
    print("First 3 characters:", file.read(3))           # "ABC"
    
    # Reposition to index 5
    file.seek(5)
    print("From index 5 to end:", file.read())           # "FGHIJ"
```

### 11.7 Working with Structured Files (CSV and JSON)

#### 1. CSV Processing (`csv` Module)
```python
import csv

# Writing CSV data using DictWriter
data_rows = [
    {"user_id": 101, "role": "admin", "active": True},
    {"user_id": 102, "role": "operator", "active": False}
]

with open("users.csv", "w", newline="", encoding="utf-8") as csv_file:
    fieldnames = ["user_id", "role", "active"]
    writer = csv.DictWriter(csv_file, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(data_rows)

# Reading CSV data using DictReader
with open("users.csv", "r", encoding="utf-8") as csv_file:
    reader = csv.DictReader(csv_file)
    for row in reader:
        print(f"ID: {row['user_id']} | Role: {row['role']}")
```

#### 2. JSON Processing (`json` Module)
```python
import json

telemetry_data = {
    "device_id": "SENSOR_404",
    "metrics": {"temp": 24.5, "humidity": 60.2},
    "alerts": []
}

# Serialization (Dict -> JSON File)
with open("telemetry.json", "w", encoding="utf-8") as json_file:
    json.dump(telemetry_data, json_file, indent=4)

# Deserialization (JSON File -> Dict)
with open("telemetry.json", "r", encoding="utf-8") as json_file:
    loaded_data = json.load(json_file)
    print("Loaded Device ID:", loaded_data["device_id"])
```

### 11.8 Exception Handling in File I/O

Defensive file handling catches specific I/O exceptions:

```python
def safe_read_file(filepath: str) -> str:
    try:
        with open(filepath, "r", encoding="utf-8") as file:
            return file.read()
    except FileNotFoundError:
        print(f"Error: Specified file '{filepath}' was not found.")
    except PermissionError:
        print(f"Error: Insufficient read permissions for '{filepath}'.")
    except UnicodeDecodeError:
        print(f"Error: Failed decoding file contents with UTF-8 encoding.")
    except IOError as e:
        print(f"I/O Error occurred: {e}")
    return ""
```

### 11.9 Section Exercises & Solutions

#### Exercise 11.1: Config File Key-Value Parser
Write a function `parse_config(filepath: str) -> dict` that reads a file formatted with `KEY=VALUE` pairs on each line (ignoring empty lines and lines starting with `#` comments) and returns a parsed dictionary.

<details>
<summary><b>View Solution</b></summary>

```python
def parse_config(filepath: str) -> dict:
    config_map = {}
    with open(filepath, "r", encoding="utf-8") as f:
        for line in f:
            stripped = line.strip()
            if not stripped or stripped.startswith("#"):
                continue
            if "=" in stripped:
                key, val = stripped.split("=", 1)
                config_map[key.strip()] = val.strip()
    return config_map

# Test creation and parsing
with open("test_settings.env", "w", encoding="utf-8") as f:
    f.write("# Environment Settings\nHOST=127.0.0.1\nPORT=5000\n\n# Security\nENABLE_AUTH=true\n")

parsed = parse_config("test_settings.env")
print("Parsed Config:", parsed)
```
</details>

---

## 12. SQLite Databases

### 12.1 Relational Database Principles and SQLite Overview

A **Relational Database Management System (RDBMS)** organizes structured data into tables consisting of rows (records) and columns (attributes).

**SQLite** is a self-contained, serverless, zero-configuration SQL database engine. Python includes standard support for SQLite through the built-in `sqlite3` module without requiring external servers or third-party packages.

### 12.2 Database Connection and Cursor Architecture

```text
┌───────────────────────┐
│     Python Script     │
└───────────┬───────────┘
            │ 1. sqlite3.connect("app.db")
            ▼
┌───────────────────────┐
│ Connection Object     │ ◄── Controls transactions (commit, rollback, close)
└───────────┬───────────┘
            │ 2. conn.cursor()
            ▼
┌───────────────────────┐
│     Cursor Object     │ ◄── Executes queries (execute, executemany, fetchall)
└───────────┬───────────┘
            │ 3. Writes/Reads
            ▼
┌───────────────────────┐
│  SQLite Database File │
└───────────────────────┘
```

### 12.3 Table Creation and Schema Constraints

SQL commands execute via the cursor's `.execute()` method:

```python
import sqlite3

# Connect to database file (or ":memory:" for an in-memory test database)
conn = sqlite3.connect("enterprise.db")
cursor = conn.cursor()

# Create table schema with relational constraints
cursor.execute("""
CREATE TABLE IF NOT EXISTS employees (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    department TEXT NOT NULL,
    salary REAL CHECK (salary > 0),
    hired_date TEXT DEFAULT CURRENT_TIMESTAMP
);
""")

conn.commit()
conn.close()
```

### 12.4 Data Manipulation Operations (CRUD)

CRUD represents the four foundational database operations:

```python
import sqlite3

conn = sqlite3.connect("enterprise.db")
cursor = conn.cursor()

# 1. CREATE (Insert Records)
cursor.execute("""
INSERT INTO employees (name, department, salary)
VALUES (?, ?, ?);
""", ("Alice Smith", "Engineering", 95000.0))

# Bulk Insertion using executemany
new_hires = [
    ("Bob Jones", "Sales", 62000.0),
    ("Charlie Brown", "Engineering", 105000.0),
    ("Diana Prince", "Security", 120000.0)
]
cursor.executemany("""
INSERT INTO employees (name, department, salary)
VALUES (?, ?, ?);
""", new_hires)
conn.commit()

# 2. READ (Query Records)
cursor.execute("SELECT id, name, department, salary FROM employees WHERE salary >= ?;", (90000.0,))
high_earners = cursor.fetchall()
print("High Earners:", high_earners)

# 3. UPDATE (Modify Existing Records)
cursor.execute("""
UPDATE employees
SET salary = salary * 1.05
WHERE department = ?;
""", ("Engineering",))
conn.commit()

# 4. DELETE (Remove Records)
cursor.execute("DELETE FROM employees WHERE name = ?;", ("Bob Jones",))
conn.commit()

conn.close()
```

### 12.5 Parameterized Queries and SQL Injection Prevention

Never construct SQL statements using raw string formatting or f-strings. Direct interpolation allows **SQL Injection** exploits:

```python
user_input_dept = "Engineering' OR '1'='1"

# ❌ VULNERABLE: Direct string interpolation (SQL Injection vulnerability)
# bad_query = f"SELECT * FROM employees WHERE department = '{user_input_dept}'"

# ✅ SECURE: Parameterized query with '?' placeholder
safe_query = "SELECT * FROM employees WHERE department = ?;"
cursor.execute(safe_query, (user_input_dept,))
```

### 12.6 Transaction Control (Commit, Rollback, Context Managers)

Database changes are staged in a transaction until committed. If an error occurs, the transaction can be rolled back to maintain consistency:

```python
import sqlite3

conn = sqlite3.connect("enterprise.db")

try:
    with conn:  # Context manager automatically commits on success or rolls back on exception
        conn.execute("UPDATE employees SET salary = salary + 500 WHERE id = 1;")
        conn.execute("UPDATE employees SET salary = salary - 500 WHERE id = 2;")
    print("Transaction successfully committed.")
except sqlite3.DatabaseError as error:
    print(f"Transaction aborted and rolled back: {error}")
finally:
    conn.close()
```

### 12.7 Row Factories (`sqlite3.Row`)

By default, SQLite queries return records as raw tuples. Setting the `row_factory` allows column access by name:

```python
import sqlite3

conn = sqlite3.connect("enterprise.db")
conn.row_factory = sqlite3.Row  # Enables dictionary-style column access
cursor = conn.cursor()

cursor.execute("SELECT id, name, salary FROM employees LIMIT 1;")
row = cursor.fetchone()

print(f"ID: {row['id']} | Name: {row['name']} | Salary: ${row['salary']:,.2f}")
conn.close()
```

### 12.8 Complete SQLite Database Manager Module

Below is a self-contained, object-oriented database manager utility:

```python
import sqlite3
from typing import List, Dict, Any, Optional

class DatabaseManager:
    def __init__(self, db_path: str = "inventory.db"):
        self.db_path = db_path
        self._init_db()

    def _get_connection(self) -> sqlite3.Connection:
        conn = sqlite3.connect(self.db_path)
        conn.row_factory = sqlite3.Row
        return conn

    def _init_db(self):
        with self._get_connection() as conn:
            conn.execute("""
            CREATE TABLE IF NOT EXISTS products (
                id INTEGER PRIMARY KEY AUTOINCREMENT,
                sku TEXT UNIQUE NOT NULL,
                name TEXT NOT NULL,
                quantity INTEGER NOT NULL CHECK (quantity >= 0),
                unit_price REAL NOT NULL CHECK (unit_price >= 0.0)
            );
            """)

    def add_product(self, sku: str, name: str, quantity: int, unit_price: float) -> int:
        with self._get_connection() as conn:
            cursor = conn.execute("""
            INSERT INTO products (sku, name, quantity, unit_price)
            VALUES (?, ?, ?, ?);
            """, (sku, name, quantity, unit_price))
            return cursor.lastrowid

    def get_all_products(self) -> List[Dict[str, Any]]:
        with self._get_connection() as conn:
            cursor = conn.execute("SELECT id, sku, name, quantity, unit_price FROM products;")
            return [dict(row) for row in cursor.fetchall()]

    def update_stock(self, sku: str, new_quantity: int) -> bool:
        with self._get_connection() as conn:
            cursor = conn.execute("UPDATE products SET quantity = ? WHERE sku = ?;", (new_quantity, sku))
            return cursor.rowcount > 0

    def delete_product(self, sku: str) -> bool:
        with self._get_connection() as conn:
            cursor = conn.execute("DELETE FROM products WHERE sku = ?;", (sku,))
            return cursor.rowcount > 0
```

### 12.9 Section Exercises & Solutions

#### Exercise 12.1: Student Grade Database
Create a script using SQLite to:
1. Create a `students` table (`id`, `name`, `score`).
2. Insert 3 student records.
3. Query and print the class average score using the SQL `AVG(score)` aggregate function.

<details>
<summary><b>View Solution</b></summary>

```python
import sqlite3

conn = sqlite3.connect(":memory:")  # In-memory test DB
cursor = conn.cursor()

cursor.execute("""
CREATE TABLE students (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    score REAL NOT NULL
);
""")

students_data = [("Alice", 92.5), ("Bob", 84.0), ("Charlie", 78.5)]
cursor.executemany("INSERT INTO students (name, score) VALUES (?, ?);", students_data)
conn.commit()

cursor.execute("SELECT AVG(score) FROM students;")
avg_score = cursor.fetchone()[0]

print(f"Class Average Score: {avg_score:.2f}")
conn.close()
```
</details>

---

## 13. GUI Development

### 13.1 Desktop GUI Architecture and `tkinter` Overview

A **Graphical User Interface (GUI)** provides visual components (windows, buttons, text fields) enabling direct visual user interaction.

Python's standard standard GUI library is **`tkinter`**, an object-oriented wrapper around the mature Tcl/Tk graphics toolkit. It requires no external package installations.

### 13.2 Application Lifecycle and the Event Loop (`mainloop`)

GUI applications are **event-driven**. The application initiates a window, constructs widgets, and enters an infinite listening loop (`mainloop()`) that responds to user inputs (clicks, keypresses, window resizing).

```python
import tkinter as tk

# 1. Instantiate root window
root = tk.Tk()
root.title("Standard GUI Application Window")
root.geometry("400x200")  # Width x Height in pixels

# 2. Add visual components
label = tk.Label(root, text="System Ready", font=("Helvetica", 14))
label.pack(pady=20)

# 3. Enter Event Loop
root.mainloop()
```

### 13.3 Core Tkinter & TTK Widgets

`tkinter.ttk` provides modern, themed widgets that integrate natively with the host OS appearance:

```text
┌─────────────────┬───────────────────────────────────────────────────────────┐
│ Widget          │ Purpose                                                   │
├─────────────────┼───────────────────────────────────────────────────────────┤
│ `tk.Label`      │ Displays static or dynamic text/images.                  │
│ `tk.Button`     │ Triggers callback actions when clicked.                  │
│ `tk.Entry`      │ Single-line text input field.                            │
│ `tk.Text`       │ Multi-line text editor supporting rich formatting.       │
│ `tk.Checkbutton`│ Toggle box for boolean states.                           │
│ `tk.Radiobutton`│ Mutually exclusive option selector.                      │
│ `tk.Frame`      │ Rectangular container grouping related widgets.          │
│ `ttk.Combobox`  │ Dropdown selection list.                                 │
└─────────────────┴───────────────────────────────────────────────────────────┘
```

### 13.4 Geometry Managers (`pack`, `grid`, `place`)

Tkinter provides three layout geometry managers:

#### 1. `pack()`: Sequential Box Packing
Packs widgets along edges (`top`, `bottom`, `left`, `right`):
```python
btn1 = tk.Button(root, text="Top Button")
btn1.pack(side="top", fill="x", padx=10, pady=5)
```

#### 2. `grid()`: Two-Dimensional Table Layout (Recommended for structured forms)
Aligns widgets into rows and columns:
```python
# Form layout example
lbl_user = tk.Label(root, text="Username:")
lbl_user.grid(row=0, column=0, sticky="w", padx=5, pady=5)

entry_user = tk.Entry(root)
entry_user.grid(row=0, column=1, padx=5, pady=5)
```

#### 3. `place()`: Absolute Pixel Positioning
Positions widgets at explicit coordinates `(x, y)`:
```python
btn_fixed = tk.Button(root, text="Fixed Button")
btn_fixed.place(x=50, y=100)
```

> [!CAUTION]
> Never mix `pack()` and `grid()` within the same parent container frame; doing so results in geometry manager collision deadlocks.

### 13.5 State Variables (`StringVar`, `IntVar`, `DoubleVar`, `BooleanVar`)

Tkinter state variables automatically synchronize widget values with underlying Python variables:

```python
import tkinter as tk

root = tk.Tk()
status_var = tk.StringVar(value="Initial Status")

def update_status():
    status_var.set("Status Updated via Callback!")

lbl = tk.Label(root, textvariable=status_var)
lbl.pack(pady=10)

btn = tk.Button(root, text="Update", command=update_status)
btn.pack()

root.mainloop()
```

### 13.6 Event Binding and Callback Mechanisms

Beyond simple button clicks, arbitrary widget events (keypresses, mouse clicks, hover motions) can be bound to handler functions using `.bind("<Event>", handler)`:

```python
import tkinter as tk

def on_key_press(event):
    print(f"Key Pressed: {event.char} (Keycode: {event.keycode})")

root = tk.Tk()
root.bind("<Key>", on_key_press)
root.mainloop()
```

### 13.7 Dialogs and Popups (`messagebox`, `filedialog`)

```python
from tkinter import messagebox, filedialog

# Display information alert
messagebox.showinfo("Operation Complete", "Database synchronized successfully.")

# Display confirmation prompt
confirmed = messagebox.askyesno("Confirm Deletion", "Are you sure you want to proceed?")

# File selection dialog
selected_file = filedialog.askopenfilename(
    title="Select Configuration File",
    filetypes=[("JSON Files", "*.json"), ("All Files", "*.*")]
)
```

### 13.8 Object-Oriented GUI Design

Encapsulating GUI code inside classes creates clean, modular, and maintainable applications:

```python
import tkinter as tk
from tkinter import ttk

class QuickCounterApp(tk.Tk):
    def __init__(self):
        super().__init__()
        self.title("State Counter")
        self.geometry("300x150")
        
        self.count = tk.IntVar(value=0)
        self._create_widgets()

    def _create_widgets(self):
        self.lbl_display = ttk.Label(self, textvariable=self.count, font=("Helvetica", 24))
        self.lbl_display.pack(pady=10)

        frame_buttons = ttk.Frame(self)
        frame_buttons.pack()

        btn_decrement = ttk.Button(frame_buttons, text="-", command=self._decrement)
        btn_decrement.pack(side="left", padx=5)

        btn_increment = ttk.Button(frame_buttons, text="+", command=self._increment)
        btn_increment.pack(side="left", padx=5)

    def _increment(self):
        self.count.set(self.count.get() + 1)

    def _decrement(self):
        self.count.set(self.count.get() - 1)

if __name__ == "__main__":
    app = QuickCounterApp()
    app.mainloop()
```

### 13.9 End-to-End Desktop Application Implementation

Below is a complete, working desktop task management system integrating **Tkinter GUI components** with an underlying **SQLite database engine**:

```python
# task_manager_gui.py
import tkinter as tk
from tkinter import ttk, messagebox
import sqlite3

class TaskDatabase:
    def __init__(self, db_name="tasks.db"):
        self.conn = sqlite3.connect(db_name)
        self.cursor = self.conn.cursor()
        self.cursor.execute("""
        CREATE TABLE IF NOT EXISTS tasks (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            title TEXT NOT NULL,
            priority TEXT NOT NULL
        );
        """)
        self.conn.commit()

    def add_task(self, title: str, priority: str):
        self.cursor.execute("INSERT INTO tasks (title, priority) VALUES (?, ?);", (title, priority))
        self.conn.commit()

    def get_all_tasks(self):
        self.cursor.execute("SELECT id, title, priority FROM tasks;")
        return self.cursor.fetchall()

    def delete_task(self, task_id: int):
        self.cursor.execute("DELETE FROM tasks WHERE id = ?;", (task_id,))
        self.conn.commit()

    def close(self):
        self.conn.close()


class TaskManagerApp(tk.Tk):
    def __init__(self):
        super().__init__()
        self.title("Task Management Desktop Manager")
        self.geometry("520x420")
        self.resizable(False, False)

        self.db = TaskDatabase()
        self._init_layout()
        self._refresh_task_list()

    def _init_layout(self):
        # Input Frame
        input_frame = ttk.LabelFrame(self, text=" Add New Task ", padding=10)
        input_frame.pack(fill="x", padx=10, pady=10)

        ttk.Label(input_frame, text="Task Description:").grid(row=0, column=0, sticky="w", padx=5, pady=5)
        self.entry_task = ttk.Entry(input_frame, width=28)
        self.entry_task.grid(row=0, column=1, padx=5, pady=5)

        ttk.Label(input_frame, text="Priority:").grid(row=0, column=2, sticky="w", padx=5, pady=5)
        self.combo_priority = ttk.Combobox(input_frame, values=["Low", "Medium", "High"], state="readonly", width=8)
        self.combo_priority.current(1)
        self.combo_priority.grid(row=0, column=3, padx=5, pady=5)

        self.btn_add = ttk.Button(input_frame, text="Add Task", command=self._add_task)
        self.btn_add.grid(row=1, column=0, columnspan=4, sticky="ew", padx=5, pady=5)

        # Task Treeview Display Frame
        list_frame = ttk.LabelFrame(self, text=" Active Tasks ", padding=10)
        list_frame.pack(fill="both", expand=True, padx=10, pady=5)

        columns = ("id", "title", "priority")
        self.tree = ttk.Treeview(list_frame, columns=columns, show="headings", selectmode="browse")
        self.tree.heading("id", text="ID")
        self.tree.heading("title", text="Task Description")
        self.tree.heading("priority", text="Priority")

        self.tree.column("id", width=40, anchor="center")
        self.tree.column("title", width=320, anchor="w")
        self.tree.column("priority", width=100, anchor="center")
        self.tree.pack(fill="both", expand=True)

        # Action Buttons Frame
        btn_frame = ttk.Frame(self, padding=5)
        btn_frame.pack(fill="x", padx=10, pady=5)

        self.btn_delete = ttk.Button(btn_frame, text="Delete Selected Task", command=self._delete_task)
        self.btn_delete.pack(side="right")

    def _add_task(self):
        title = self.entry_task.get().strip()
        priority = self.combo_priority.get()

        if not title:
            messagebox.showwarning("Validation Error", "Task description cannot be empty.")
            return

        self.db.add_task(title, priority)
        self.entry_task.delete(0, tk.END)
        self._refresh_task_list()

    def _delete_task(self):
        selected_item = self.tree.selection()
        if not selected_item:
            messagebox.showinfo("Selection Required", "Please select a task from the list to delete.")
            return

        task_values = self.tree.item(selected_item, "values")
        task_id = int(task_values[0])
        self.db.delete_task(task_id)
        self._refresh_task_list()

    def _refresh_task_list(self):
        for item in self.tree.get_children():
            self.tree.delete(item)
        for task in self.db.get_all_tasks():
            self.tree.insert("", tk.END, values=task)

    def destroy(self):
        self.db.close()
        super().destroy()

if __name__ == "__main__":
    app = TaskManagerApp()
    app.mainloop()
```

### 13.10 Section Exercises & Solutions

#### Exercise 13.1: Temperature Converter GUI
Build a Tkinter application that accepts a temperature in Celsius from an `Entry` widget, converts it to Fahrenheit ($F = C \times \frac{9}{5} + 32$) when a `Button` is pressed, and displays the result in a `Label`. Handle non-numeric input gracefully with `messagebox.showerror`.

<details>
<summary><b>View Solution</b></summary>

```python
import tkinter as tk
from tkinter import ttk, messagebox

def convert_temp():
    raw_val = entry_celsius.get().strip()
    try:
        celsius = float(raw_val)
        fahrenheit = (celsius * 9/5) + 32
        lbl_result.config(text=f"Fahrenheit: {fahrenheit:.2f} °F")
    except ValueError:
        messagebox.showerror("Invalid Input", "Please enter a valid numeric temperature value.")

root = tk.Tk()
root.title("Celsius to Fahrenheit Converter")
root.geometry("320x160")
root.resizable(False, False)

frame = ttk.Frame(root, padding=15)
frame.pack(fill="both", expand=True)

ttk.Label(frame, text="Enter Celsius (°C):").grid(row=0, column=0, sticky="w", pady=5)
entry_celsius = ttk.Entry(frame, width=12)
entry_celsius.grid(row=0, column=1, sticky="w", pady=5)

btn_convert = ttk.Button(frame, text="Convert", command=convert_temp)
btn_convert.grid(row=1, column=0, columnspan=2, sticky="ew", pady=10)

lbl_result = ttk.Label(frame, text="Fahrenheit: --", font=("Helvetica", 11, "bold"))
lbl_result.grid(row=2, column=0, columnspan=2, pady=5)

if __name__ == "__main__":
    root.mainloop()
```
</details>
