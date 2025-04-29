# Python Async Comprehension

A project focused on asynchronous generators and comprehensions in Python, demonstrating practical applications of Python's async features.

## Project Overview

This project explores the implementation of asynchronous generators and async comprehensions in Python. It includes three tasks that demonstrate how to create and use async generators, how to collect results using async comprehensions, and how to measure the runtime of parallel async operations.

## Requirements

### General
- **Allowed editors**: `vi`, `vim`, `emacs`
- **Environment**: All files will be interpreted/compiled on Ubuntu 18.04 LTS using `python3` (version 3.7)
- **File format**: All files should end with a new line
- **Shebang line**: The first line of all files should be exactly `#!/usr/bin/env python3`
- **README.md**: A README.md file at the root of the project folder is mandatory
- **Coding style**: Code should follow the `pycodestyle` style (version 2.5.x)
- **File length**: The length of files will be tested using `wc`
- **Documentation**: 
  - All modules must have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
  - All functions must have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`)
  - Documentation should be a real sentence explaining the purpose of the module, class, or method
- **Type annotations**: All functions and coroutines must be type-annotated

## Tasks

### 0. Async Generator
- **File**: `0-async_generator.py`
- **Description**: Write a coroutine called `async_generator` that takes no arguments.
- **Details**:
  - The coroutine will loop 10 times
  - Each time it will asynchronously wait 1 second
  - Then yield a random number between 0 and 10
  - Use the `random` module

### 1. Async Comprehensions
- **File**: `1-async_comprehension.py`
- **Description**: Import `async_generator` from the previous task and write a coroutine called `async_comprehension` that takes no arguments.
- **Details**:
  - The coroutine will collect 10 random numbers using an async comprehension over `async_generator`
  - Return the 10 random numbers

### 2. Run time for four parallel comprehensions
- **File**: `2-measure_runtime.py`
- **Description**: Import `async_comprehension` from the previous file and write a `measure_runtime` coroutine.
- **Details**:
  - Execute `async_comprehension` four times in parallel using `asyncio.gather`
  - Measure the total runtime and return it
  - The total runtime should be roughly 10 seconds

## Understanding the Runtime

In Task 2, despite running four async comprehensions in parallel, the total runtime is still approximately 10 seconds. This is because each async comprehension collects values from the async generator which has 10 iterations with a 1-second delay each. When run in parallel, these operations happen concurrently, not simultaneously, so the total time is determined by the longest operation, which is approximately 10 seconds.

## Repository Structure

- **GitHub repository**: `alx-backend-python`
- **Directory**: `0x02-python_async_comprehension`
- **Files**:
  - `0-async_generator.py`
  - `1-async_comprehension.py`
  - `2-measure_runtime.py`
