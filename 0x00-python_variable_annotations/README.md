# Python Variable Annotations

This project explores the use of type annotations in Python 3, focusing on specifying function signatures and variable types according to the Python Enhancement Proposal (PEP) 484.

## Overview

Type annotations in Python are a way to document the expected types of function parameters, return values, and variables. While Python remains dynamically typed, these annotations help with:

- Code documentation
- IDE support for type checking
- Runtime type checking via external tools like mypy
- Better code maintenance and readability

## Project Info

- **Language**: Python 3.7
- **Style Guide**: pycodestyle 2.5
- **Environment**: Ubuntu 18.04 LTS

## Requirements

### General

- Allowed editors: vi, vim, emacs
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3.7
- All files should end with a new line
- The first line of all files should be exactly `#!/usr/bin/env python3`
- All code should use the pycodestyle style (version 2.5)
- All files must be executable
- All modules, classes and functions must be documented:
  - Module documentation: `python3 -c 'print(__import__("my_module").__doc__)'`
  - Class documentation: `python3 -c 'print(__import__("my_module").MyClass.__doc__)'`
  - Function documentation: `python3 -c 'print(__import__("my_module").my_function.__doc__)'`
- Documentation should be real sentences explaining the purpose of the module, class, or method

## Tasks

### 0. Basic annotations - add
- File: `0-add.py`
- Description: Write a type-annotated function `add` that takes two float arguments and returns their sum as a float.

### 1. Basic annotations - concat
- File: `1-concat.py`
- Description: Write a type-annotated function `concat` that takes two string arguments and returns a concatenated string.

### 2. Basic annotations - floor
- File: `2-floor.py`
- Description: Write a type-annotated function `floor` that takes a float argument and returns the floor of the float as an integer.

### 3. Basic annotations - to string
- File: `3-to_str.py`
- Description: Write a type-annotated function `to_str` that takes a float argument and returns its string representation.

### 4. Define variables
- File: `4-define_variables.py`
- Description: Define and annotate variables with specified values:
  - `a`: an integer with value 1
  - `pi`: a float with value 3.14
  - `i_understand_annotations`: a boolean with value True
  - `school`: a string with value "ALX"

### 5. Complex types - list of floats
- File: `5-sum_list.py`
- Description: Write a type-annotated function `sum_list` that takes a list of floats and returns their sum as a float.

### 6. Complex types - mixed list
- File: `6-sum_mixed_list.py`
- Description: Write a type-annotated function `sum_mixed_list` that takes a list of integers and floats and returns their sum as a float.

### 7. Complex types - string and int/float to tuple
- File: `7-to_kv.py`
- Description: Write a type-annotated function `to_kv` that takes a string and an int/float, and returns a tuple containing the string and the square of the number as a float.

### 8. Complex types - functions
- File: `8-make_multiplier.py`
- Description: Write a type-annotated function `make_multiplier` that takes a float and returns a function that multiplies a float by the given multiplier.

### 9. Duck typing - iterable object
- File: `9-element_length.py`
- Description: Annotate a function's parameters and return values with appropriate types for a function that returns a list of tuples containing sequence and their length.

### 10. Duck typing - first element of a sequence (Advanced)
- File: `100-safe_first_element.py`
- Description: Add correct duck-typed annotations to a function that safely returns the first element of a sequence.

### 11. More involved type annotations (Advanced)
- File: `101-safely_get_value.py`
- Description: Add type annotations to a function that safely gets a value from a dictionary using TypeVar.

### 12. Type Checking (Advanced)
- File: `102-type_checking.py`
- Description: Use mypy to validate a piece of code and apply necessary changes.

## Resources

For more information on Python type annotations, refer to:
- [PEP 484 -- Type Hints](https://peps.python.org/pep-0484/)
- [Python typing module](https://docs.python.org/3/library/typing.html)
- [mypy documentation](http://mypy-lang.org/)
