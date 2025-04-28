# Python Async Function

This project explores asynchronous programming in Python using `async`/`await` syntax and the `asyncio` library. It includes implementations of various asynchronous functions, coroutines, and tasks.

## Requirements

### General
- **Python Version**: 3.7
- **OS**: Ubuntu 18.04 LTS
- **Style Guide**: pycodestyle 2.5.x
- **Editors**: vi, vim, emacs
- **Shebang**: All files must start with `#!/usr/bin/env python3`
- **Documentation**: All modules and functions must be documented
- **Type Annotations**: All functions and coroutines must be type-annotated

## Project Tasks

### 0. The basics of async
**File**: `0-basic_async_syntax.py`

Implement an asynchronous coroutine `wait_random` that takes an integer argument `max_delay` (with default value of 10) and waits for a random delay between 0 and `max_delay` seconds before returning the delay value.

```python
#!/usr/bin/env python3

import asyncio

wait_random = __import__('0-basic_async_syntax').wait_random

print(asyncio.run(wait_random()))
print(asyncio.run(wait_random(5)))
print(asyncio.run(wait_random(15)))
```

Example output:
```
9.034261504534394
1.6216525464615306
10.634589756751769
```

### 1. Let's execute multiple coroutines at the same time with async
**File**: `1-concurrent_coroutines.py`

Implement an async routine `wait_n` that takes two integer arguments: `n` and `max_delay`. It should spawn `wait_random` `n` times with the specified `max_delay` and return a list of all delays in ascending order.

```python
#!/usr/bin/env python3

import asyncio

wait_n = __import__('1-concurrent_coroutines').wait_n

print(asyncio.run(wait_n(5, 5)))
print(asyncio.run(wait_n(10, 7)))
print(asyncio.run(wait_n(10, 0)))
```

Example output:
```
[0.9693881173832269, 1.0264573845731002, 1.7992690129519855, 3.641373003434587, 4.500011569340617]
[0.07256214141415429, 1.518551245602588, 3.355762808432721, 3.7032593997182923, 3.7796178143655546, 4.744537840582318, 5.50781365463315, 5.758942587637626, 6.109707751654879, 6.831351588271327]
[0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]
```

### 2. Measure the runtime
**File**: `2-measure_runtime.py`

Create a `measure_time` function that takes integers `n` and `max_delay` as arguments, measures the total execution time for `wait_n(n, max_delay)`, and returns `total_time / n` as a float.

```python
#!/usr/bin/env python3

measure_time = __import__('2-measure_runtime').measure_time

n = 5
max_delay = 9

print(measure_time(n, max_delay))
```

Example output:
```
1.759705400466919
```

### 3. Tasks
**File**: `3-tasks.py`

Write a function `task_wait_random` using regular function syntax that takes an integer `max_delay` and returns an `asyncio.Task` object.

```python
#!/usr/bin/env python3

import asyncio

task_wait_random = __import__('3-tasks').task_wait_random

async def test(max_delay: int) -> float:
    task = task_wait_random(max_delay)
    await task
    print(task.__class__)

asyncio.run(test(5))
```

Example output:
```
<class '_asyncio.Task'>
```

### 4. Tasks
**File**: `4-tasks.py`

Create a function `task_wait_n` that is nearly identical to `wait_n` except it calls `task_wait_random` instead of `wait_random`.

```python
#!/usr/bin/env python3

import asyncio

task_wait_n = __import__('4-tasks').task_wait_n

n = 5
max_delay = 6
print(asyncio.run(task_wait_n(n, max_delay)))
```

Example output:
```
[0.2261658205652346, 1.1942770588220557, 1.8410422186086628, 2.1457353803430523, 4.002505454641153]
```

## Resources

For more information on asynchronous programming in Python, refer to:

- [Python asyncio documentation](https://docs.python.org/3/library/asyncio.html)
- [Async IO in Python: A Complete Walkthrough](https://realpython.com/async-io-python/)
- [Random Module in Python](https://docs.python.org/3/library/random.html)
- [asyncio - Asynchronous I/O](https://docs.python.org/3/library/asyncio.html)
- [random.uniform](https://docs.python.org/3/library/random.html#random.uniform)
