# Functions and Modules
## Python-First Course Material
**Software Engineering Diploma · Year 1, Term 1 · Foundations**

> **Course approach:** Python is the primary teaching language throughout this material. JavaScript is included only in a short comparison appendix where it helps connect these concepts to the diploma's web-development projects.

---

## Course overview

### Why this course matters

A small program can be written in one file, but as it grows, repeated code and mixed responsibilities make it difficult to understand, test, debug, and extend. This course teaches you to divide a program into **functions** and **modules**.

- A **function** is a named, reusable unit of work.
- A **module** is a Python file that groups related code.
- A **package** is a folder that groups related modules.
- A **test** checks whether a piece of code behaves as expected.

By the end of this course, you should be able to design useful functions, validate input, test your logic, organise a small Python project into modules, and build a command-line inventory application.

### Learning outcomes

You should be able to:

1. Explain function definitions, calls, parameters, arguments, return values, and side effects.
2. Write functions with required, default, keyword-only, and flexible arguments.
3. Explain local and global scope, variable lifetime, and shadowing.
4. Use tuples, unpacking, type hints, and docstrings appropriately.
5. Pass functions to other functions and use `lambda`, `sorted`, `map`, `filter`, and comprehensions.
6. Explain the call stack, recursion, base cases, and closures.
7. Design small, readable, testable functions with clear responsibilities.
8. Validate data and raise meaningful errors.
9. Write automated tests with `pytest`.
10. Import code from modules and organise code into packages.
11. Build and test a modular inventory program.
12. Use Git to record small, working changes.

### Prerequisite knowledge

You should already know basic variables, strings, numbers, lists, dictionaries, comparisons, `if` statements, loops, and simple input/output in Python. If a topic depends on one of these, the material briefly reviews it.

### How to use this guide

1. Read the explanation before studying the code.
2. Type each example yourself rather than only copying it.
3. Predict the output before running the code.
4. Change the inputs and explain why the output changes.
5. Write pseudocode for exercises before translating it into Python.
6. Commit each small, working improvement with Git.

---

# Part 0 — Setup and Working Habits

## 0.1 Tools

You need:

- Python 3.10 or newer
- VS Code or another code editor
- A terminal
- Git
- `pytest` for automated testing

Check Python:

```bash
python --version
```

On some systems, use:

```bash
python3 --version
```

Check Git:

```bash
git --version
```

## 0.2 Run a Python file

Create `hello.py`:

```python
print("Hello, Python!")
```

Run it from the terminal:

```bash
python hello.py
```

If your system uses `python3`, run `python3 hello.py`.

**What happens?** Python reads the file and executes its statements from top to bottom. `print()` displays text in the terminal.

## 0.3 Start a Git repository

Run these commands inside your project folder:

```bash
git init
git add .
git commit -m "Start functions and modules course"
```

- `git init` creates a Git repository.
- `git add .` stages the current changes.
- `git commit` saves a snapshot with a description.

Use meaningful commit messages such as `Add calculate_total function` or `Test invalid inventory items`.

## 0.4 Use a `.gitignore` file

Create a file named `.gitignore`:

```gitignore
__pycache__/
.venv/
.pytest_cache/
inventory.json
```

These entries tell Git to ignore generated Python files, the virtual environment, test cache, and the sample inventory data file. Do not ignore source code or tests.

---

# Part 1 — Understanding Functions

## 1.1 The problem functions solve

Imagine a shop that adds a 7.5% charge to a product's price. Without a function, the calculation might be repeated:

```python
rice_total = 85000 + 85000 * 0.075
garri_total = 9500 + 9500 * 0.075
beans_total = 48000 + 48000 * 0.075
```

The arithmetic works, but the rule is repeated. If the rate changes, each copy must be found and updated.

This violates the spirit of **DRY: Don't Repeat Yourself**. When the same rule appears in several places, those copies can drift apart.

A function lets us write the rule once:

```python
def add_charge(price, rate=0.075):
    return price * (1 + rate)


print(add_charge(85000))
print(add_charge(9500))
print(add_charge(48000))
```

The same function handles different prices.

> The numbers and rate in this example are teaching values, not tax advice. Real tax rules should be verified before being used in a live application.

## 1.2 What is a function?

A function is a named block of code that performs a particular task and can be called whenever that task is needed.

Think of a function as a recipe:

- **Name:** what the recipe is called.
- **Inputs:** ingredients supplied to it.
- **Body:** instructions to follow.
- **Output:** the result, if it returns one.

Python uses `def` to define a function.

```python
def greet():
    print("Welcome!")
```

This defines a function named `greet`. It does **not** execute the body yet.

Call it like this:

```python
greet()
```

Output:

```text
Welcome!
```

The parentheses `()` are part of the call syntax. They tell Python to call the function.

## 1.3 Understand each part of a function

```python
def add_numbers(first, second):
    result = first + second
    return result


answer = add_numbers(4, 6)
print(answer)
```

Line by line:

1. `def` starts a function definition.
2. `add_numbers` is the function's name.
3. `first` and `second` are **parameters**: named placeholders for incoming values.
4. The colon `:` marks the beginning of the function body.
5. The indented line `result = first + second` adds the two values and stores the sum.
6. `return result` sends the result back to the caller and ends the function.
7. `add_numbers(4, 6)` calls the function with the arguments `4` and `6`.
8. The returned value, `10`, is assigned to `answer`.
9. `print(answer)` displays `10`.

Output:

```text
10
```

### Parameter versus argument

- **Parameter:** the name in the function definition, such as `first`.
- **Argument:** the actual value passed to the function, such as `4`.

```python
def greet_person(name):  # name is a parameter
    return f"Hello, {name}!"


message = greet_person("Ada")  # "Ada" is an argument
print(message)
```

## 1.4 Defining a function versus calling it

```python
def say_hello():
    print("Hello")


print("Before")
say_hello()
print("After")
```

Output:

```text
Before
Hello
After
```

Python executes the top-level statements in order. When it reaches `say_hello()`, it enters the function, runs its body, and then returns to the next top-level statement.

**Common mistake:** defining a function and expecting it to run automatically. A normal function definition creates the function; a call runs it.

## 1.5 `print()` versus `return`

These do different jobs.

- `print(value)` displays a value to the user.
- `return value` sends a value back to the code that called the function.

```python
def show_total(a, b):
    print(a + b)


def get_total(a, b):
    return a + b


x = show_total(2, 3)
print("x =", x)

y = get_total(2, 3) * 10
print("y =", y)
```

Output:

```text
5
x = None
y = 50
```

Why is `x` `None`? `show_total()` prints `5`, but it does not return a value. Python functions return `None` when they finish without a `return` value.

`get_total()` returns `5`, so the caller can multiply it by `10`.

**Rule:** use `return` for calculations and reusable logic. Use `print()` when displaying output is the function's intended job.

## 1.6 `return` ends the function

```python
def check_number(number):
    if number < 0:
        return "Negative"

    return "Zero or positive"


print(check_number(-3))
print(check_number(8))
```

Once Python executes a `return`, the function stops. Statements after that return in the same execution path do not run.

## 1.7 Functions that make decisions

A function can apply rules, not just perform arithmetic.

```python
def grade(score):
    if score < 0 or score > 100:
        raise ValueError("Score must be between 0 and 100")

    if score >= 70:
        return "A"
    if score >= 60:
        return "B"
    if score >= 50:
        return "C"
    if score >= 45:
        return "D"
    if score >= 40:
        return "E"

    return "F"


print(grade(72))
print(grade(49))
print(grade(12))
```

Output:

```text
A
D
F
```

New terms:

- `if` checks a condition.
- `or` means at least one of the conditions must be true.
- `raise` signals an error.
- `ValueError` is commonly used when a value has the correct general type but is not acceptable.
- A **guard clause** checks an invalid or exceptional case early and stops it from continuing.

The grade function checks invalid scores first. If the score is valid, it checks the grade boundaries from highest to lowest.

**Boundary testing matters.** Test `69` and `70`, for example, because a small comparison mistake can put a student in the wrong grade.

### Part 1 practice

1. Write `square(number)` that returns the number multiplied by itself.
2. Write `is_even(number)` that returns `True` for even numbers and `False` for odd numbers.
3. Write `calculate_delivery(subtotal, fee)` that returns the subtotal plus the fee.
4. Write a `grade(score)` function using the ranges above. What should happen for `-1` and `101`?
5. Explain in your own words why `print()` and `return` are not interchangeable.

---

# Part 2 — Parameters and Arguments in Python

## 2.1 Required parameters

```python
def multiply(first, second):
    return first * second


print(multiply(4, 5))
```

Both arguments are required. Calling `multiply(4)` raises a `TypeError` because the second argument is missing.

## 2.2 Default arguments

A default argument is used when the caller does not supply a value for that parameter.

```python
def add_delivery_fee(price, fee=1500):
    return price + fee


print(add_delivery_fee(10000))
print(add_delivery_fee(10000, 2500))
```

Output:

```text
11500
12500
```

In the first call, Python uses the default fee of `1500`. In the second call, `2500` replaces the default.

Parameters without defaults normally come before parameters with defaults:

```python
def describe_item(name, price=0):
    return f"{name}: ₦{price}"
```

This is valid. A required parameter after a default parameter is generally invalid:

```python
# Invalid:
# def describe_item(price=0, name):
#     ...
```

## 2.3 Positional arguments

A positional argument is matched to a parameter by its position.

```python
def describe_person(name, age):
    return f"{name} is {age} years old."


print(describe_person("Ada", 24))
```

`"Ada"` goes to `name`; `24` goes to `age`.

Positional arguments are concise, but long calls can become difficult to read when several arguments have similar types.

## 2.4 Keyword arguments

A keyword argument names the parameter receiving the value.

```python
def describe_product(name, price, in_stock=True, currency="₦"):
    status = "in stock" if in_stock else "out of stock"
    return f"{name}: {currency}{price:,.2f} ({status})"


print(describe_product(
    name="Rice 50kg",
    price=85000,
    in_stock=False,
))
```

Output:

```text
Rice 50kg: ₦85,000.00 (out of stock)
```

Keyword arguments make calls easier to read. They also allow arguments to be supplied in a different order when the function's rules permit it.

## 2.5 Keyword-only parameters and `*`

A bare `*` in a function's parameter list makes the parameters after it keyword-only.

```python
def describe_product(name, price, *, in_stock=True, currency="₦"):
    status = "in stock" if in_stock else "out of stock"
    return f"{name}: {currency}{price:,.2f} ({status})"


print(describe_product("Rice", 85000, in_stock=False))
```

The `in_stock` and `currency` parameters must be supplied by name if the caller supplies them.

This call is invalid:

```python
# describe_product("Rice", 85000, False, "$")
```

Keyword-only parameters are useful when a function has options that would be confusing if supplied by position.

## 2.6 Collecting extra positional arguments with `*args`

Sometimes a function needs to accept any number of values.

```python
def average(*scores):
    if not scores:
        raise ValueError("Provide at least one score")

    return sum(scores) / len(scores)


print(average(70, 65, 80))
```

Output:

```text
71.66666666666667
```

`*scores` collects all extra positional arguments into a tuple.

- `sum(scores)` adds the values.
- `len(scores)` counts them.
- The function rejects an empty set of scores to avoid dividing by zero.

The name `scores` is not special. The asterisk is what gives the parameter its behaviour; `*args` is simply a common naming convention.

### Unpacking a list

```python
scores = [70, 65, 80]

print(average(*scores))
```

The `*` in the call unpacks the list into separate positional arguments. This is different from the `*scores` in a function definition, which collects arguments.

## 2.7 Collecting extra keyword arguments with `**kwargs`

```python
def log_event(message, **details):
    print(message)
    print(details)


log_event("Order placed", order_id=42, total=18500)
```

Output:

```text
Order placed
{'order_id': 42, 'total': 18500}
```

`**details` collects extra keyword arguments into a dictionary.

Use this when a function genuinely needs flexible named options. Do not use it merely to avoid deciding what parameters a function needs.

### Unpacking a dictionary

```python
options = {
    "order_id": 42,
    "total": 18500,
}

log_event("Order placed", **options)
```

The `**` in the call unpacks dictionary entries into keyword arguments.

## 2.8 Returning multiple values

Python can return several values using a tuple.

```python
def min_max(numbers):
    return min(numbers), max(numbers)


result = min_max([45, 82, 67])
print(result)

low, high = min_max([45, 82, 67])
print(low)
print(high)
```

Output:

```text
(45, 82)
45
82
```

Technically, `return min(numbers), max(numbers)` returns one tuple containing two values. The assignment `low, high = ...` unpacks the tuple into two variables.

This is useful when a calculation naturally produces a small group of related results.

## 2.9 The mutable default argument trap

This is a major Python pitfall.

```python
def add_item_bad(item, basket=[]):
    basket.append(item)
    return basket


print(add_item_bad("rice"))
print(add_item_bad("beans"))
```

Output:

```text
['rice']
['rice', 'beans']
```

Why did the second call keep `"rice"`? Python creates the default list when it defines the function, not afresh on every call. The same list is reused.

### Correct approach

```python
def add_item(item, basket=None):
    if basket is None:
        basket = []

    basket.append(item)
    return basket


print(add_item("rice"))
print(add_item("beans"))
```

Output:

```text
['rice']
['beans']
```

`None` is used as a signal that no basket was provided. The function then creates a new list.

**Rule:** avoid mutable default values such as `[]`, `{}`, and `set()` when you intend each call to have fresh data.

## 2.10 Parameter quick reference

| Syntax | Meaning |
|---|---|
| `def f(a, b):` | Two required parameters |
| `def f(a, b=10):` | `b` has a default value |
| `def f(*args):` | Collect extra positional arguments into a tuple |
| `def f(**kwargs):` | Collect extra keyword arguments into a dictionary |
| `def f(a, *, b):` | `b` must be passed by keyword |
| `f(*values)` | Unpack an iterable into positional arguments |
| `f(**options)` | Unpack a mapping into keyword arguments |

### Part 2 practice

1. Write `calculate_total(price, quantity, discount=0)` that returns the total after a percentage discount.
2. Write `sum_all(*numbers)` that returns the sum of any number of arguments.
3. Write `build_profile(name, **details)` that returns a dictionary containing the name and supplied details.
4. Write a function returning the smallest and largest numbers in a list.
5. Fix a function that uses `items=[]` as a default argument.

---

# Part 3 — Scope, Lifetime, and Names

## 3.1 What is scope?

**Scope** is the part of a program where a variable or name can be accessed.

A local variable is created inside a function and is normally available only within that function.

```python
def calculate_discount(price):
    discount = price * 0.10
    return price - discount


print(calculate_discount(10000))
```

The variable `discount` is local to `calculate_discount`.

This will fail:

```python
# print(discount)
```

The name `discount` does not exist in the surrounding scope.

## 3.2 Global variables

A global variable is defined outside a function.

```python
discount_rate = 0.10


def final_price(price):
    discount = price * discount_rate
    return price - discount


print(final_price(10000))
```

The function can read `discount_rate` from the surrounding global scope.

Global variables can be useful for true constants, but functions that secretly depend on or modify global state are harder to reuse and test.

## 3.3 Avoid changing globals unnecessarily

Consider:

```python
total = 0


def add_to_total(amount):
    global total
    total += amount
```

This function changes a variable outside itself. The caller must know that `total` will be changed.

A clearer design passes the current total in and returns the new total:

```python
def add_to_total(total, amount):
    return total + amount


total = 0
total = add_to_total(total, 500)
total = add_to_total(total, 300)

print(total)
```

Output:

```text
800
```

The function's dependencies are visible in its parameters, and its result is explicit.

## 3.4 Shadowing

Shadowing occurs when a name in an inner scope hides a name with the same name in an outer scope.

```python
name = "Global name"


def show_name():
    name = "Local name"
    print(name)


show_name()
print(name)
```

Output:

```text
Local name
Global name
```

The assignment inside the function creates a local variable. It does not replace the global variable.

## 3.5 Variable lifetime

A local variable is available while its relevant scope is active. When the function finishes, the local name is no longer accessible from outside the function.

However, an object created inside a function can remain alive if another reference still points to it. The important distinction is between the **name's scope** and the **object's lifetime**.

## 3.6 Python's enclosing scope and `nonlocal`

A nested function is a function defined inside another function.

```python
def make_counter():
    count = 0

    def increment():
        nonlocal count
        count += 1
        return count

    return increment


counter = make_counter()
print(counter())
print(counter())
print(counter())
```

Output:

```text
1
2
3
```

`nonlocal count` tells Python that `increment` should update the `count` variable in the nearest enclosing function scope, rather than create a new local variable.

This example also introduces **closures**, which are explained in Part 6.

---

# Part 4 — Functions as Values

## 4.1 Functions can be stored in variables

In Python, a function is an object. You can assign it to another name.

```python
def greet(name):
    return f"Hello, {name}"


say_hello = greet

print(say_hello("Ada"))
```

Notice that `say_hello = greet` has no parentheses. It assigns the function itself. `greet("Ada")` would call the function.

## 4.2 Passing a function to another function

A function that accepts another function or returns a function is called a **higher-order function**.

```python
def apply_to_all(items, operation):
    return [operation(item) for item in items]


def square(number):
    return number * number


print(apply_to_all([1, 2, 3], square))
```

Output:

```text
[1, 4, 9]
```

`operation` receives a function. Inside the list comprehension, `operation(item)` calls that function for each item.

## 4.3 Lambda functions

A `lambda` creates a small anonymous function, usually for a short expression.

```python
double = lambda number: number * 2

print(double(5))
```

Output:

```text
10
```

The equivalent named function is often clearer:

```python
def double(number):
    return number * 2
```

Use a lambda for a short, simple operation. Use `def` when the logic needs several statements, documentation, validation, or a meaningful reusable name.

## 4.4 Sorting with a function

```python
products = [
    {"name": "Rice", "price": 85000},
    {"name": "Garri", "price": 9500},
    {"name": "Charger", "price": 3500},
]


cheapest_first = sorted(products, key=lambda product: product["price"])

print(cheapest_first)
```

`sorted()` returns a new sorted list. Its `key` parameter accepts a function that calculates the value used to compare each item.

Here, the lambda returns each product's price.

A named alternative:

```python
def get_price(product):
    return product["price"]


cheapest_first = sorted(products, key=get_price)
```

## 4.5 `map()`, `filter()`, and comprehensions

### `map()`: transform every item

```python
numbers = [1, 2, 3]

squares = list(map(lambda number: number * number, numbers))

print(squares)
```

Output:

```text
[1, 4, 9]
```

`map()` applies a function to each item. In Python 3 it returns an iterator, so `list()` is used here to collect the results into a list.

A list comprehension is often easier to read:

```python
squares = [number * number for number in numbers]
```

### `filter()`: keep items that pass a test

```python
numbers = [3, 9, 4, 12, 7]

large_numbers = list(filter(lambda number: number >= 8, numbers))

print(large_numbers)
```

Output:

```text
[9, 12]
```

The function passed to `filter()` should return a truthy or falsy result for each item.

The equivalent comprehension is:

```python
large_numbers = [number for number in numbers if number >= 8]
```

### List comprehension with a condition

```python
products = [
    {"name": "Rice", "price": 85000},
    {"name": "Garri", "price": 9500},
    {"name": "Charger", "price": 3500},
]

affordable_names = [
    product["name"]
    for product in products
    if product["price"] < 10000
]

print(affordable_names)
```

Output:

```text
['Garri', 'Charger']
```

Read it as: “Create a list of each product's name for every product whose price is below 10,000.”

## 4.6 `reduce()` and accumulation

Python's `functools.reduce()` repeatedly combines values into one result. For ordinary totals, `sum()` is usually clearer.

```python
from functools import reduce

numbers = [10, 20, 30]

total = reduce(lambda accumulated, number: accumulated + number, numbers, 0)

print(total)
```

Output:

```text
60
```

The initial value `0` is the starting accumulated total. Each iteration combines that total with the next number.

Prefer:

```python
total = sum(numbers)
```

when the task is simply adding numbers.

## 4.7 When should you use each tool?

| Tool | Typical use |
|---|---|
| List comprehension | Build a new list with transformations or conditions |
| `sorted()` | Create a sorted list |
| `map()` | Apply a transformation function |
| `filter()` | Keep items passing a condition |
| `sum()` | Add numbers |
| `reduce()` | Combine items using a general accumulation rule |
| `lambda` | A short function used locally |

### Part 4 practice

1. Use a list comprehension to create the squares of numbers from 1 to 10.
2. Filter a list of prices to keep only values below ₦10,000.
3. Sort dictionaries representing students by score.
4. Write a function that accepts a list and a transformation function.
5. Rewrite a complicated lambda as a named function.

---

# Part 5 — Type Hints, Docstrings, and Validation

## 5.1 Type hints

Type hints document the kinds of values a function expects and returns.

```python
def add_numbers(first: int, second: int) -> int:
    return first + second
```

- `first: int` says that `first` is intended to be an integer.
- `second: int` says the same for `second`.
- `-> int` says the function is intended to return an integer.

Python does not automatically enforce these annotations at runtime. Editors, linters, and type-checking tools can use them to detect likely mistakes.

A type hint is documentation and tooling support, not a substitute for validating untrusted input.

## 5.2 Common type annotations

```python
def format_naira(amount: float) -> str:
    return f"₦{amount:,.2f}"
```

Examples:

| Annotation | Meaning |
|---|---|
| `str` | Text |
| `int` | Integer |
| `float` | Floating-point number |
| `bool` | `True` or `False` |
| `list[str]` | List intended to contain strings |
| `dict[str, int]` | Dictionary with string keys and integer values |
| `str | None` | A string or `None` |

For more complex types, Python's `typing` module provides tools such as `Callable`, `Sequence`, and `TypedDict`.

## 5.3 Docstrings

A docstring describes what a function, class, or module does.

```python
def format_naira(amount: float) -> str:
    """Format an amount with a naira symbol and two decimal places."""
    return f"₦{amount:,.2f}"
```

The string immediately inside the function body is its docstring.

You can inspect it:

```python
help(format_naira)
```

Good documentation explains purpose, important assumptions, parameters, return values, and errors when those details are not obvious.

## 5.4 Validate inputs

Do not assume all callers will provide acceptable data.

```python
def apply_discount(price: float, percent: float) -> float:
    """Return the price after a percentage discount."""
    if price < 0:
        raise ValueError("Price cannot be negative")

    if not 0 <= percent <= 100:
        raise ValueError("Discount must be between 0 and 100")

    return price * (1 - percent / 100)
```

Examples:

```python
print(apply_discount(10000, 10))
print(apply_discount(10000, 0))
print(apply_discount(10000, 100))
```

Output:

```text
9000.0
10000.0
0.0
```

Validation prevents impossible values from silently entering the program.

For user input, remember that `input()` returns text. Convert it to a number and handle conversion errors when necessary:

```python
raw_price = input("Enter price: ")

try:
    price = float(raw_price)
except ValueError:
    print("Please enter a valid number.")
else:
    print(f"You entered ₦{price:,.2f}")
```

This is an introductory example. Error handling is studied more deeply in the next course.

---

# Part 6 — The Call Stack, Recursion, and Closures

## 6.1 The call stack

When Python calls a function, it keeps track of that function's active execution. Nested calls create a stack of active calls.

Think of a stack of plates: the most recently added plate is the first one removed.

```python
def calculate_vat(price):
    return price * 0.075


def total_with_vat(price):
    vat = calculate_vat(price)
    return price + vat


print(total_with_vat(1000))
```

Execution sequence:

1. Python calls `total_with_vat(1000)`.
2. That function calls `calculate_vat(1000)`.
3. `calculate_vat` returns `75`.
4. Its call finishes and Python resumes `total_with_vat`.
5. `total_with_vat` calculates `1000 + 75` and returns `1075`.
6. `print()` displays `1075.0`.

The call stack helps explain tracebacks. A traceback shows the chain of calls that led to an error. Read the final error line first to identify the error type and message, then inspect the relevant call locations.

## 6.2 Recursion

Recursion occurs when a function calls itself to solve a smaller version of a problem.

Every sound recursive function needs:

1. A **base case** that stops the recursion.
2. A **recursive case** that moves towards the base case.

```python
def factorial(number):
    if number < 0:
        raise ValueError("Factorial is not defined here for negative integers")

    if number == 0:
        return 1

    return number * factorial(number - 1)


print(factorial(5))
```

Output:

```text
120
```

The calculation is:

- `factorial(5)` = `5 * factorial(4)`
- `factorial(4)` = `4 * factorial(3)`
- `factorial(3)` = `3 * factorial(2)`
- `factorial(2)` = `2 * factorial(1)`
- `factorial(1)` = `1 * factorial(0)`
- `factorial(0)` returns `1` — the base case.

The values then return back up the call stack: `1`, `1`, `2`, `6`, `24`, `120`.

### A recursion mistake

```python
# Do not run this:
# def infinite(number):
#     return infinite(number + 1)
```

This never reaches a stopping condition. Python eventually raises `RecursionError`.

Use recursion when it makes the problem clearer. A loop is often simpler for straightforward repetition. Algorithms and recursion are covered in more depth later in the diploma.

## 6.3 Closures

A closure is a function that retains access to variables from the scope where it was created, even after the outer function has finished.

```python
def make_discount(percent):
    def discount(price):
        return price * (1 - percent / 100)

    return discount


ten_percent_off = make_discount(10)
twenty_percent_off = make_discount(20)

print(ten_percent_off(20000))
print(twenty_percent_off(20000))
```

Output:

```text
18000.0
16000.0
```

How it works:

1. `make_discount(10)` runs with `percent` set to `10`.
2. It defines the inner `discount` function.
3. It returns that inner function without calling it.
4. `ten_percent_off` now refers to the returned function.
5. The returned function retains access to `percent`, which is `10`.
6. Calling `ten_percent_off(20000)` calculates the discounted price.

The closure lets each returned function retain a different discount rate.

## 6.4 A counter closure

```python
def make_counter():
    count = 0

    def increment():
        nonlocal count
        count += 1
        return count

    return increment


counter = make_counter()

print(counter())
print(counter())
print(counter())
```

Output:

```text
1
2
3
```

The inner function retains access to `count`. The `nonlocal` statement allows it to update the variable from the enclosing function.

Closures are useful for small pieces of retained state, function factories, and callbacks. Do not use them when a simple parameter or ordinary data structure would be clearer.

### Part 6 practice

1. Trace `factorial(4)` by writing down every call and return.
2. Fix a recursive function that never reaches its base case.
3. Write `make_multiplier(factor)` that returns a function multiplying a number by that factor.
4. Explain why two functions created by `make_discount(10)` and `make_discount(20)` behave differently.
5. Describe the difference between scope and lifetime.

---

# Part 7 — Designing Good Functions

## 7.1 One function, one clear responsibility

A good function has a name that describes its job and does not take responsibility for unrelated tasks.

Poor design:

```python
def process_order(items, customer_type):
    # Calculate prices.
    # Apply discounts.
    # Print the receipt.
    # Save an order file.
    # Send a notification.
    ...
```

This function has too many reasons to change. Testing its calculations also requires dealing with output and file operations.

A better design separates the tasks:

```python
def calculate_subtotal(items):
    return sum(item["price"] * item["quantity"] for item in items)


def apply_customer_discount(total, customer_type):
    if customer_type == "student":
        return total * 0.90

    return total


def format_receipt(customer_name, total):
    return f"Receipt for {customer_name}: ₦{total:,.2f}"
```

Each function has one main job.

## 7.2 Naming functions

Prefer descriptive verb phrases:

| Unclear | Better |
|---|---|
| `data()` | `load_items()` |
| `stuff()` | `calculate_total()` |
| `check()` | `is_valid_email()` |
| `thing()` | `format_receipt()` |
| `process()` | `validate_order()` |

Useful naming patterns include:

- `get_...` or `find_...` for retrieving something.
- `is_...`, `has_...`, or `can_...` for questions returning Boolean values.
- `calculate_...` for calculations.
- `format_...` for presentation.
- `validate_...` for checking data.
- `create_...`, `add_...`, `update_...`, and `delete_...` for data operations.

## 7.3 Pure functions and side effects

A **pure function** has two defining properties:

1. The same inputs always produce the same output.
2. It does not cause observable changes outside itself.

```python
def calculate_total(price, quantity):
    return price * quantity
```

Calling this function with `100` and `3` always returns `300`. It does not print, write a file, or change global state.

A function with a side effect might print a message, save a file, modify external state, or communicate with a network service.

```python
def save_message(path, message):
    with open(path, "w", encoding="utf-8") as file:
        file.write(message)
```

This function changes a file. Its effect is outside its return value.

Side effects are necessary in real applications. The goal is not to eliminate them, but to keep them separate from calculations and business rules where practical.

## 7.4 Do not modify input data unexpectedly

This function changes the list supplied by the caller:

```python
def add_item_bad(items, new_item):
    items.append(new_item)
    return items
```

A caller might not expect the original list to change.

An alternative that returns a new list is:

```python
def add_item(items, new_item):
    return [*items, new_item]
```

The expression `[*items, new_item]` creates a new list containing the original elements and the new item. It does not append to the original list.

This is a shallow copy. If the list contains mutable nested objects, those objects are still shared unless copied separately.

## 7.5 Validate and fail clearly

```python
def apply_discount(price, percent):
    if price < 0:
        raise ValueError("Price cannot be negative")

    if not 0 <= percent <= 100:
        raise ValueError("Discount must be between 0 and 100")

    return price * (1 - percent / 100)
```

Failing clearly is better than silently returning a misleading result.

Validate data at the appropriate boundary, especially when it comes from a user, file, network request, or external service.

## 7.6 Refactoring

**Refactoring** means improving code structure without intentionally changing its behaviour.

Before:

```python
def order_total(items, customer_type):
    total = 0

    for item in items:
        total += item["price"] * item["quantity"]

    if customer_type == "student":
        total = total * 0.9

    print(f"Total: ₦{total:,.2f}")
```

After:

```python
def calculate_subtotal(items):
    return sum(item["price"] * item["quantity"] for item in items)


def apply_discount(total, customer_type):
    return total * 0.9 if customer_type == "student" else total


def order_total(items, customer_type):
    subtotal = calculate_subtotal(items)
    return apply_discount(subtotal, customer_type)


def show_order_total(items, customer_type):
    total = order_total(items, customer_type)
    print(f"Total: ₦{total:,.2f}")
```

Now the calculation can be tested without capturing printed output. The display function is responsible for presentation.

## 7.7 Practical design checklist

Before accepting a function, ask:

- Does it have one clear responsibility?
- Does its name describe what it does?
- Are its parameters necessary and understandable?
- Does it return results when callers need to reuse them?
- Does it validate important assumptions?
- Does it avoid unexpected changes to inputs and global variables?
- Is its documentation useful?
- Can its important behaviour be tested?

---

# Part 8 — Automated Testing with `pytest`

## 8.1 What is a test?

A test runs code with known inputs and checks whether the result matches the expected behaviour.

Tests help detect regressions: bugs introduced while changing code that previously worked.

Install `pytest`:

```bash
python -m pip install pytest
```

Create `grades.py`:

```python
def grade(score):
    if not 0 <= score <= 100:
        raise ValueError("Score must be between 0 and 100")

    if score >= 70:
        return "A"
    if score >= 60:
        return "B"
    if score >= 50:
        return "C"
    if score >= 45:
        return "D"
    if score >= 40:
        return "E"

    return "F"
```

## 8.2 Write tests

Create `test_grades.py`:

```python
import pytest

from grades import grade


def test_grade_a():
    assert grade(70) == "A"
    assert grade(100) == "A"


def test_grade_boundaries():
    assert grade(69) == "B"
    assert grade(59) == "C"
    assert grade(44) == "F"


def test_rejects_invalid_score():
    with pytest.raises(ValueError):
        grade(101)
```

Run:

```bash
python -m pytest
```

Explanation:

- `import pytest` loads the testing tool.
- `from grades import grade` imports the function being tested.
- Test functions conventionally begin with `test_`.
- `assert actual == expected` checks whether two values are equal.
- `pytest.raises(ValueError)` checks that the code raises the expected error.

If an assertion fails, the test runner reports the failure.

## 8.3 What should you test?

Test more than the happy path:

1. A normal, valid input.
2. Boundary values such as `69` and `70`.
3. Empty collections where relevant.
4. Invalid values.
5. Error conditions.
6. Important combinations of inputs.

Functions that return values and avoid unnecessary side effects are generally easier to test.

---

# Part 9 — Python Modules and Packages

## 9.1 Why modules?

A module is a Python file containing code that can be imported by another file.

Instead of placing every function in one giant file, separate related responsibilities.

For example:

```text
shop/
    main.py
    pricing.py
    inventory.py
    formatting.py
```

- `pricing.py` contains price calculations.
- `inventory.py` contains inventory rules.
- `formatting.py` contains display-formatting helpers.
- `main.py` connects the pieces and starts the program.

This makes code easier to find, reuse, test, and maintain.

## 9.2 Create your own module

Create `helpers.py`:

```python
def double(number):
    return number * 2


def square(number):
    return number * number
```

Create `main.py` in the same directory:

```python
import helpers

print(helpers.double(5))
print(helpers.square(5))
```

Output:

```text
10
25
```

`import helpers` makes the module available under the name `helpers`. The dot in `helpers.double` means “the `double` function belonging to the `helpers` module.”

## 9.3 Different import styles

```python
import helpers

print(helpers.double(5))
```

Or import one name:

```python
from helpers import double

print(double(5))
```

Or rename an imported name:

```python
from helpers import double as double_number

print(double_number(5))
```

Use `import module` when seeing the origin of a name makes the code clearer. Use selective imports when they improve readability without hiding where important names came from.

Avoid `from helpers import *`. It imports names without making their origin clear and can create name collisions.

## 9.4 The `__name__ == "__main__"` pattern

A Python file can be executed directly or imported by another file.

```python
def double(number):
    return number * 2


if __name__ == "__main__":
    print(double(4))
```

When run directly, Python sets `__name__` to `"__main__"`, so the print statement runs.

When another file imports this module, the condition is false and the print statement does not run.

This allows a file to provide reusable functions while also having a small demonstration or command-line entry point.

## 9.5 Standard-library modules

Python includes modules that do not need to be installed separately.

| Module | Purpose | Example |
|---|---|---|
| `math` | Mathematical operations | `math.sqrt(81)` |
| `random` | Random choices and numbers | `random.choice(["A", "B"])` |
| `datetime` | Dates and times | `datetime.date.today()` |
| `json` | JSON encoding and decoding | `json.dumps(data)` |
| `pathlib` | File-system paths | `Path("data.json")` |
| `statistics` | Basic statistics | `statistics.mean([1, 2, 3])` |
| `collections` | Useful container types | `Counter(items)` |

Example:

```python
import statistics

scores = [70, 65, 80, 90]

print(statistics.mean(scores))
```

## 9.6 Packages

A package groups related modules into a directory.

Example structure:

```text
inventory/
    __init__.py
    service.py
    validators.py
    storage.py
```

- `service.py` contains inventory rules.
- `validators.py` checks input.
- `storage.py` handles reading and writing data.
- `__init__.py` can define the package's public interface.

For a conventional package, `__init__.py` is useful for making the package structure explicit, although Python also supports namespace packages without it.

Example `inventory/__init__.py`:

```python
from .service import add_item, update_item, delete_item

__all__ = ["add_item", "update_item", "delete_item"]
```

The leading dot means “import from this package.”

## 9.7 Virtual environments and dependencies

A virtual environment isolates installed packages for a particular project.

Create one:

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

Install a package:

```bash
python -m pip install pytest
```

Record dependencies if needed:

```bash
python -m pip freeze > requirements.txt
```

A teammate can install those recorded packages with:

```bash
python -m pip install -r requirements.txt
```

Commit `requirements.txt` when it is part of the project's dependency workflow. Do not commit `.venv/`.

## 9.8 Avoid circular imports

A circular import occurs when module A imports module B while module B also imports module A.

This creates a confusing dependency relationship and can cause partially initialised module errors.

A common solution is to move the shared function or data into a third module that both modules can import. If two modules constantly depend on each other, reconsider their responsibilities.

## 9.9 Organising modules

A practical structure for a small Python application:

```text
src/
    main.py
    inventory/
        __init__.py
        service.py
        validators.py
        storage.py
        formatting.py
tests/
    test_inventory.py
```

A useful dependency direction is:

```text
main.py
  └── inventory service
        ├── validators
        └── storage interface
```

Keep dependencies understandable. Low-level utility functions should not need to import the application's entry point.

---

# Part 10 — Main Course Project: Shop Inventory CLI

This is the primary project for applying the course in Python. It teaches reusable functions, validation, modules, file storage, testing, and separation of responsibilities.

## 10.1 Project requirements

Build a command-line inventory program that can:

- Add a product.
- List products.
- Search by product name.
- Update a product's price.
- Delete a product.
- Calculate total stock value.
- Save data to a JSON file.
- Validate product information.
- Report errors clearly.
- Test business rules without running the interactive menu.

## 10.2 Suggested folder structure

```text
inventory-cli/
    main.py
    inventory.json
    inventory/
        __init__.py
        validators.py
        service.py
        storage.py
    tests/
        test_service.py
```

`inventory.json` is generated data. Add it to `.gitignore` if you do not want local inventory records in Git.

## 10.3 The data model

Represent each product as a dictionary:

```python
item = {
    "id": 1,
    "name": "Rice 50kg",
    "price": 85000,
    "quantity": 12,
}
```

- `id` uniquely identifies the item in this small example.
- `name` is its product name.
- `price` is its unit price.
- `quantity` is the number of units in stock.

The stock value for this product is `price * quantity`.

For production financial systems, money should be modelled carefully, commonly in integer minor units such as kobo, or with an appropriate decimal representation. Floating-point numbers can introduce rounding errors.

## 10.4 `inventory/validators.py`

```python
def validate_item(name, price, quantity):
    """Return a list of validation messages; an empty list means valid."""
    errors = []

    if not isinstance(name, str) or not name.strip():
        errors.append("Name is required")

    if isinstance(price, bool) or not isinstance(price, (int, float)):
        errors.append("Price must be numeric")
    elif price <= 0:
        errors.append("Price must be greater than zero")

    if isinstance(quantity, bool) or not isinstance(quantity, int):
        errors.append("Quantity must be a whole number")
    elif quantity < 0:
        errors.append("Quantity cannot be negative")

    return errors
```

The validator returns a list rather than printing messages. An empty list means there are no validation errors.

The explicit Boolean checks matter because `bool` is a subclass of `int` in Python. Without those checks, `True` could be accepted as a price or quantity.

## 10.5 `inventory/service.py`

```python
from .validators import validate_item


def add_item(items, name, price, quantity):
    """Return a new inventory list containing the added item."""
    errors = validate_item(name, price, quantity)

    if errors:
        raise ValueError("; ".join(errors))

    next_id = max((item["id"] for item in items), default=0) + 1

    new_item = {
        "id": next_id,
        "name": name.strip(),
        "price": price,
        "quantity": quantity,
    }

    return [*items, new_item]


def find_items(items, search_text=""):
    """Find product names containing the search text, ignoring case."""
    needle = search_text.strip().casefold()

    return [
        item for item in items
        if needle in item["name"].casefold()
    ]


def total_value(items):
    """Calculate the total value of all stock."""
    return sum(
        item["price"] * item["quantity"]
        for item in items
    )


def update_item(items, item_id, changes):
    """Return a new inventory list with one item updated."""
    existing = next(
        (item for item in items if item["id"] == item_id),
        None,
    )

    if existing is None:
        raise KeyError(f"No item with id {item_id}")

    allowed_fields = {"name", "price", "quantity"}
    unknown_fields = set(changes) - allowed_fields

    if unknown_fields:
        raise ValueError(
            f"Cannot update fields: {', '.join(sorted(unknown_fields))}"
        )

    updated_data = {**existing, **changes}
    errors = validate_item(
        updated_data["name"],
        updated_data["price"],
        updated_data["quantity"],
    )

    if errors:
        raise ValueError("; ".join(errors))

    updated_data["name"] = updated_data["name"].strip()

    return [
        updated_data if item["id"] == item_id else item
        for item in items
    ]


def delete_item(items, item_id):
    """Return a new inventory list without the selected item."""
    if not any(item["id"] == item_id for item in items):
        raise KeyError(f"No item with id {item_id}")

    return [item for item in items if item["id"] != item_id]
```

Important concepts in this module:

- `from .validators import validate_item` imports a helper from the same package.
- The service functions contain inventory rules, not terminal input/output.
- `max(..., default=0)` supports an empty inventory.
- `next(generator, None)` finds the first matching item or returns `None`.
- `{**existing, **changes}` creates a dictionary using the existing values and then replaces values provided in `changes`.
- List comprehensions build new lists without changing the original list.
- `raise` makes invalid operations fail clearly.

This is a teaching project, not a multi-user database. The simple ID strategy is adequate for the exercise but is not a substitute for a database-generated identifier in a concurrent production system.

## 10.6 `inventory/storage.py`

```python
import json
from pathlib import Path


def load_items(path):
    """Load inventory from JSON; return an empty list if no file exists."""
    file_path = Path(path)

    if not file_path.exists():
        return []

    with file_path.open("r", encoding="utf-8") as file:
        return json.load(file)


def save_items(path, items):
    """Save inventory to a JSON file."""
    file_path = Path(path)

    with file_path.open("w", encoding="utf-8") as file:
        json.dump(items, file, indent=2)
```

The `json` module converts between Python data and JSON text.

- `json.load(file)` reads JSON from an open file.
- `json.dump(items, file, indent=2)` writes JSON with readable indentation.
- `Path` represents a file-system path.

This starter version allows malformed JSON and file permission errors to surface. In a later error-handling lesson, improve the program to report corrupted files and failed saves clearly rather than silently discarding data.

## 10.7 `inventory/__init__.py`

```python
from .service import (
    add_item,
    update_item,
    delete_item,
    find_items,
    total_value,
)

__all__ = [
    "add_item",
    "update_item",
    "delete_item",
    "find_items",
    "total_value",
]
```

This gives other files a clear set of public functions to import from the package.

## 10.8 Test the service layer

Create `tests/test_service.py`:

```python
import pytest

from inventory import (
    add_item,
    update_item,
    delete_item,
    find_items,
    total_value,
)


def test_add_item_returns_new_list():
    original = []

    result = add_item(original, "Rice 50kg", 85000, 12)

    assert original == []
    assert result == [
        {
            "id": 1,
            "name": "Rice 50kg",
            "price": 85000,
            "quantity": 12,
        }
    ]


def test_add_item_rejects_invalid_data():
    with pytest.raises(ValueError, match="Name is required"):
        add_item([], "   ", 100, 1)


def test_find_items_ignores_case():
    items = add_item([], "Rice 50kg", 85000, 12)

    assert len(find_items(items, "RICE")) == 1


def test_total_value():
    items = add_item([], "A", 100, 2)
    items = add_item(items, "B", 50, 4)

    assert total_value(items) == 400


def test_update_item():
    items = add_item([], "Garri", 9500, 40)

    updated = update_item(items, 1, {"price": 10000})

    assert updated[0]["price"] == 10000
    assert items[0]["price"] == 9500


def test_delete_item():
    items = add_item([], "Garri", 9500, 40)

    assert delete_item(items, 1) == []

    with pytest.raises(KeyError):
        delete_item(items, 99)
```

Run the tests from the project root:

```bash
python -m pytest
```

These tests focus on business rules and do not require a terminal menu or JSON file. This is one of the key benefits of separating service logic from input/output.

## 10.9 Build the command-line interface

The final step is to create `main.py`. Its job is to:

1. Load saved data.
2. Show a menu.
3. Read user choices.
4. Call service functions.
5. Save successful changes.
6. Display results and errors.

This file is intentionally kept separate from `service.py`. The interactive menu should coordinate the program rather than contain all its business logic.

**Extension task:** implement the menu only after the service functions and tests pass. Start with listing and adding items, then add search, update, delete, and total stock value.

---

# Part 11 — Applying the Course to the Diploma Projects

## 11.1 Personal portfolio website

The portfolio is a web project, so browser interactions will ultimately use JavaScript. The function-design principles from this Python-first course still apply.

Separate responsibilities such as:

- Project data.
- Date and text formatting.
- Project filtering.
- Contact-form validation.
- Theme selection.
- Screen rendering.

The important transferable idea is to separate pure rules from browser effects. Python examples teach the principle first; JavaScript implements the browser-specific behaviour.

## 11.2 Simple CRUD application

CRUD means:

- **Create:** add a record.
- **Read:** display or search records.
- **Update:** change a record.
- **Delete:** remove a record.

The Python inventory project practises these same operations without requiring a browser. Once the concepts are understood, the JavaScript web application can use the same structure: validation, business rules, storage, rendering, and an entry point.

---

# Part 12 — Git Workflow for the Course

Use Git throughout the project rather than waiting until the end.

A simple workflow:

```bash
git status
git add inventory/service.py tests/test_service.py
git commit -m "Add inventory service and tests"
```

- `git status` shows changed files.
- `git add` stages the files you want to include.
- `git commit` records a snapshot of those changes.

Make small commits after meaningful working steps. Avoid committing secrets, virtual environments, caches, or generated local data.

---

# Part 13 — Common Errors and How to Diagnose Them

| Error or symptom | Common cause | First thing to check |
|---|---|---|
| `NameError` | A name is misspelled or outside scope | Check spelling and where the name is defined |
| `TypeError` about a missing argument | The function call omitted a required argument | Compare the call with the function definition |
| Function returns `None` | It printed the result or omitted `return` | Check the return path |
| `UnboundLocalError` | A function assigns to a name Python treats as local before it has a value | Pass the value in and return the updated result |
| A list keeps growing between calls | A mutable default argument is being reused | Replace `items=[]` with `items=None` and create a fresh list |
| `ZeroDivisionError` | The denominator is zero | Validate empty input or zero denominators |
| `RecursionError` | Recursion does not reach its base case | Check whether each recursive call gets closer to the stopping condition |
| `ModuleNotFoundError` | Wrong environment, module name, or installation | Check the active interpreter and file layout |
| `ImportError` involving a partially initialised module | Possible circular import | Move shared code to a third module |
| `FileNotFoundError` | A path does not point to an existing file | Check the working directory and path |
| `JSONDecodeError` | The file is empty or contains invalid JSON | Inspect the saved file and decide how corruption should be handled |

### A debugging routine

1. Read the exception type and message.
2. Find the line identified by the traceback.
3. Inspect the values passed into that line.
4. Reduce the problem to a small reproducible example.
5. Fix the cause, not just the visible symptom.
6. Add a test if the problem could return.

---

# Part 14 — Practice Exercises

Write pseudocode first, then implement each exercise in Python.

## Beginner

1. `is_even(number)` returns whether a number is even.
2. `count_vowels(text)` returns the number of vowels in a string.
3. `celsius_to_fahrenheit(celsius)` converts Celsius to Fahrenheit.
4. `calculate_area(length, width)` returns the area of a rectangle.
5. `format_naira(amount)` returns a formatted naira string.
6. `find_maximum(numbers)` returns the largest number or raises a clear error for an empty list.

## Intermediate

7. `total_with_delivery(prices, delivery_fee=1500, free_above=50000)` adds a delivery fee unless the subtotal qualifies for free delivery.
8. `make_multiplier(factor)` returns a function that multiplies a number by `factor`.
9. `is_palindrome(text)` checks whether text reads the same forward and backward, ignoring case, spaces, and punctuation.
10. `fizzbuzz(limit)` returns a list from 1 to `limit`, replacing multiples of 3 with `"Fizz"`, multiples of 5 with `"Buzz"`, and multiples of both with `"FizzBuzz"`.
11. Create a `shipping.py` module with `shipping_fee(city, weight_kg)`. For this exercise, Lagos costs ₦1,500 plus ₦200 per kg; other cities cost ₦3,500 plus ₦450 per kg. Import and test it from another file.
12. Refactor a long function from an earlier assignment into at least four smaller functions.

## Testing and debugging

Find and fix the problems in these examples.

```python
def average(numbers):
    total = 0

    for number in numbers:
        total += number

    return total / len(numbers)


print(average([]))
```

The empty list causes division by zero. Decide on a clear rule, such as raising `ValueError`.

```python
def add_tag(tag, tags=[]):
    tags.append(tag)
    return tags
```

The default list is reused across calls. Use `None` as the default and create a new list inside the function.

```python
def total(prices):
    sum(prices)
```

The function calculates a sum but does not return it.

---

# Part 15 — Review Questions and Answers

## Questions

1. What is the difference between a parameter and an argument?
2. What does a Python function return if it reaches the end without returning a value?
3. Why is `return` different from `print()`?
4. Why can a mutable default argument cause unexpected behaviour?
5. What do `*args` and `**kwargs` collect?
6. What is the difference between local and global scope?
7. What is a pure function?
8. What two parts does a recursive function need?
9. What is a closure?
10. What is a module?
11. What is the purpose of `if __name__ == "__main__":`?
12. Why should business rules be tested independently of the command-line menu?
13. What is the difference between a package and a module?
14. Why are circular imports a design problem?
15. What is refactoring?
16. Why should invalid input produce a clear error?

## Suggested answers

1. A parameter is a named placeholder in a function definition; an argument is the value passed in a call.
2. `None`.
3. `print()` displays a value; `return` sends a value back to the caller for reuse.
4. The default mutable object is created once when the function is defined and can be shared across calls.
5. `*args` collects extra positional arguments into a tuple; `**kwargs` collects extra keyword arguments into a dictionary.
6. A local name is available within its relevant local scope. A global name is defined at module level and can be accessed from functions under Python's name-resolution rules.
7. A pure function returns the same result for the same inputs and causes no observable external side effects.
8. A base case and a recursive case that progresses towards it.
9. A function that retains access to variables from the scope where it was created.
10. A Python file containing code that can be imported by other code.
11. It runs the guarded block when the file is executed directly, rather than when imported.
12. Independent tests run faster, isolate failures, and do not require interactive input/output.
13. A module is a file; a package groups related modules.
14. Circular imports create dependencies in both directions and can cause partially initialised modules or confusing architecture.
15. Refactoring improves code structure without intentionally changing behaviour.
16. Clear errors prevent invalid values from silently producing misleading results and make problems easier to diagnose.

---

# Part 16 — Glossary

| Term | Plain-language meaning |
|---|---|
| Function | Reusable block of code with a name |
| Definition | Creating a function |
| Call | Running a function |
| Parameter | Placeholder in a function definition |
| Argument | Value passed to a function |
| Return value | Value sent back to the caller |
| Side effect | Change or external action beyond returning a value |
| Scope | Where a name can be accessed |
| Local variable | Name available in a local scope |
| Global variable | Name defined at module level |
| Shadowing | An inner name hiding an outer name |
| Default argument | Value used when an argument is omitted |
| Keyword argument | Argument passed by parameter name |
| `*args` | Collects extra positional arguments |
| `**kwargs` | Collects extra keyword arguments |
| Tuple | Ordered, immutable collection of values |
| Unpacking | Assigning values from a collection to separate names |
| Lambda | Small anonymous function expression |
| Callback | Function passed to other code to be called |
| Higher-order function | Function that accepts or returns functions |
| Type hint | Annotation describing intended input or output types |
| Docstring | Documentation string attached to a function or module |
| Pure function | Function with predictable output and no external side effects |
| Call stack | Active chain of function calls |
| Recursion | Function calling itself |
| Base case | Condition that stops recursion |
| Closure | Function retaining access to its enclosing variables |
| Validation | Checking whether data meets requirements |
| Exception | Object signalling an error or unusual condition |
| Unit test | Automated check of a small piece of code |
| Refactoring | Improving structure without intentionally changing behaviour |
| Module | Python file containing code |
| Package | Group of related modules |
| Import | Making names from another module available |
| Dependency | Code or package a program relies on |
| Virtual environment | Isolated Python package environment |
| Entry point | Place where an application starts |
| CRUD | Create, Read, Update, Delete |
| DRY | Don't Repeat Yourself |

---

# Part 17 — Where This Course Leads

This course prepares you for:

- **Debugging and Error Handling:** tracebacks, exceptions, and reliable error recovery.
- **Data Structures:** organising and processing collections of data.
- **Algorithms and Recursion:** problem-solving strategies and computational reasoning.
- **Object-Oriented Programming:** organising behaviour and state into classes.
- **SOLID principles:** applying responsibility and dependency design principles at a broader level.
- **Web and API development:** separating validation, business rules, storage, and presentation.

## Final habit

Whenever a function grows too large or the same logic appears in multiple places, ask:

1. What is this code's single responsibility?
2. What should the function be called?
3. What information should it receive as parameters?
4. What should it return?
5. Which module should own it?
6. How can I test it independently?

That habit is the foundation of maintainable software.
