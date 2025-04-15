---
id: 20250405-cs-missing-semester
aliases:
  - CS-Missing-Semester
tags: []
---

# CS-Missing-Semester

[regex101: build, test, and debug regex](https://regex101.com/r/qqbZqh/2)

- regex debug

awk is a programming language
[How to Find or Validate an Email Address](https://www.regular-expressions.info/email.html)
[Idiomatic awk « \1](https://backreference.org/2010/02/10/idiomatic-awk/)
html:
[ericchiang/pup: Parsing HTML at the command line](https://github.com/EricChiang/pup)

- jq , yq etc

python pprint

# Debug

assert and print is a great way
unit test

- could also use logger

better gdb
[pwndbg/pwndbg: Exploit Development and Reverse Engineering with GDB & LLDB Made Easy](https://github.com/pwndbg/pwndbg)
[🐛 LLDB](https://lldb.llvm.org/)

for network:
tcpdump, wireshark

chrome/firefox tools and js repl

python:
ipdb

b 6 -> breakpoint6
p locals() -> show all the variable in python

- Static analysis
- pyflakes
  - nvim get this

# static-analysis

[analysis-tools-dev/static-analysis: ⚙️ A curated list of static analysis (SAST) tools and linters for all programming languages, config files, build tools, and more. The focus is on tools which improve code quality.](https://github.com/analysis-tools-dev/static-analysis)

[mtshiba/pylyzer: A fast, feature-rich static code analyzer & language server for Python](https://github.com/mtshiba/pylyzer)

- pylint, pyright, pytype, etc.?
- ruff as well

# Profiling (how to optimize the code)

[How do Ruby & Python profilers work?](https://jvns.ca/blog/2017/12/17/how-do-ruby---python-profilers-work-/)

# adding timer

![](20250405-cs-missing-semester/2025-04-05-03-02-15.png)
time difference -> optimize

Let’s dive into this code snippet from your MIT course, which is part of a lecture on timing and debugging in Python. The code demonstrates how to measure the time taken by a piece of code (in this case, a `time.sleep` call) using the `time` module. I’ll explain what the code does, how it helps with debugging, and the core concept of timing in programming. I’ll also provide tips for tracing variables, since you mentioned earlier that this can be challenging.

---

### What the Code Does

The code measures how long a specific operation (sleeping for a duration) takes to execute. Here’s the code with proper formatting:

```python
import time

# Get current time
start = time.time()

# Do some work
n = 1000  # Assume n is defined
print("Sleeping for {} s".format(n/1000))
time.sleep(n/1000)

# Compute time between start and now
print(time.time() - start)
```

- **Line 1**: `start = time.time()`
  - Records the current time (in seconds since the Unix epoch, January 1, 1970) as the starting point.
- **Line 2-3**: `print("Sleeping for {} s".format(n/1000))` and `time.sleep(n/1000)`
  - Prints a message indicating how long the program will sleep (e.g., for `n = 1000`, it sleeps for 1 second).
  - `time.sleep(n/1000)` pauses the program for `n/1000` seconds (e.g., 1 second).
- **Line 4**: `print(time.time() - start)`
  - Computes the elapsed time by subtracting the start time from the current time and prints it.

**Output Example** (for `n = 1000`):

```
Sleeping for 1.0 s
1.00123456789  # Elapsed time in seconds
```

---

### Core Concept: Timing for Debugging

The core concept here is **timing**—measuring how long a piece of code takes to run. This is a fundamental debugging and performance analysis technique in programming.

#### First Principles: Why Measure Time?

- **Debugging**: If a program is slow, you need to identify which part is taking too long.
- **Performance Optimization**: Timing helps you compare different approaches to see which is faster.
- **Validation**: Ensures that operations (like sleeping) behave as expected.

**Analogy**: Imagine you’re cooking a meal, and it’s taking too long. You use a stopwatch to time each step (chopping, boiling, baking) to find the bottleneck. Timing in code is like using that stopwatch to measure each operation.

---

### How This Timer Helps with Debugging

Let’s break down how this specific timer (`time.time() - start`) helps with debugging:

#### 1. **Verifies Expected Behavior**

- The code sleeps for `n/1000` seconds (e.g., 1 second for `n = 1000`).
- By measuring the elapsed time, you can confirm that `time.sleep` is working as expected:
  - Expected: Elapsed time ≈ 1 second.
  - If the elapsed time is much different (e.g., 0.1 seconds or 10 seconds), something is wrong (e.g., `n` is incorrect, or `time.sleep` isn’t behaving as expected).

**Example**:

- If `n = 1000`, you expect to sleep for 1 second.
- Output: `1.00123456789` seconds—close to 1 second, so `time.sleep` is working correctly.
- If the output were `0.1` seconds, you’d debug: Is `n` wrong? Is `time.sleep` broken?

#### 2. **Identifies Performance Issues**

- If you replace `time.sleep(n/1000)` with a real operation (e.g., a loop, a function call, or a database query), timing helps you see if it’s too slow.
- Example: If a function takes 10 seconds but you expect 1 second, you know to investigate that function.

**Modified Example**:

```python
start = time.time()
# Simulate a slow operation
total = 0
for i in range(1000000):
    total += i
print(time.time() - start)
```

- If this takes 0.5 seconds, you might decide to optimize the loop (e.g., use `sum(range(1000000))`).

#### 3. **Compares Different Implementations**

- Timing lets you compare two approaches to see which is faster.
- Example: If you have two ways to compute a sum, time both:

  ```python
  start = time.time()
  total = sum(range(1000000))
  print("Sum:", time.time() - start)

  start = time.time()
  total = 0
  for i in range(1000000):
      total += i
  print("Loop:", time.time() - start)
  ```

- Output might show `sum` is faster, helping you choose the better method.

#### 4. **Detects Unexpected Delays**

- If the elapsed time is much longer than expected, it might indicate:
  - A bug (e.g., an infinite loop, a slow API call).
  - System issues (e.g., the computer is overloaded, slowing down `time.sleep`).
- In this code, if `time.sleep(1)` takes 5 seconds, you’d investigate: Is the system busy? Is there a bug?

#### 5. **Helps with Logging and Monitoring**

- This timer pairs well with the logging concepts from the previous section. You can log the time taken for operations to monitor performance over time.
- Example:

  ```python
  import logging
  logging.basicConfig(level=logging.INFO)
  logger = logging.getLogger("Timer")

  start = time.time()
  time.sleep(1)
  elapsed = time.time() - start
  logger.info(f"Sleep took {elapsed} seconds")
  ```

---

### How This Fits into Debugging

- **Debugging Context**: The lecture is likely teaching you tools to diagnose issues in your code. Timing is one such tool, alongside logging (from the previous section).
- **Why `time.sleep`?**: It’s a simple example to demonstrate timing. In real debugging, you’d time more complex operations (e.g., file I/O, network requests, computations).
- **Instructor’s Point**: The slide text (“it from the original time and by doing this you can end of narrow”) suggests narrowing down performance issues. Timing helps you “narrow down” which part of your code is slow.

---

### Tips for Tracing Variables in This Code

Since you mentioned tracing variables like `n` was hard, let’s trace the variables here (`start`, `n`, elapsed time) using a table and some of the tips we discussed earlier.

#### Code with `n` Defined

```python
import time

n = 1000  # Define n
start = time.time()
print("Sleeping for {} s".format(n/1000))
time.sleep(n/1000)
print(time.time() - start)
```

#### Step 1: Identify Variables

- `n`: The number of milliseconds to sleep (divided by 1000 to get seconds).
- `start`: The starting time (from `time.time()`).
- `time.time() - start`: The elapsed time.

#### Step 2: Trace with a Table

Let’s assume `time.time()` starts at 1000.0 seconds (a simplified value for clarity).

| Step                  | `n`  | `start` | `time.time()` | Action                      | Elapsed Time (`time.time() - start`) |
| --------------------- | ---- | ------- | ------------- | --------------------------- | ------------------------------------ |
| Before `start`        | 1000 | -       | 1000.0        | -                           | -                                    |
| After `start`         | 1000 | 1000.0  | 1000.0        | `start = time.time()`       | -                                    |
| After `print`         | 1000 | 1000.0  | 1000.0        | Prints "Sleeping for 1.0 s" | -                                    |
| After `time.sleep(1)` | 1000 | 1000.0  | 1001.0        | Sleeps for 1 second         | 1001.0 - 1000.0 = 1.0                |
| Final `print`         | 1000 | 1000.0  | 1001.0        | Prints elapsed time         | 1.0                                  |

- **Notes**:
  - `time.time()` increases by 1 second during `time.sleep(1)`.
  - The elapsed time matches the expected sleep duration, confirming the code works as intended.

#### Step 3: Add Print Statements

To make tracing easier, you could add prints:

```python
n = 1000
print(f"n = {n}")
start = time.time()
print(f"start = {start}")
print("Sleeping for {} s".format(n/1000))
time.sleep(n/1000)
end = time.time()
print(f"end = {end}")
print(end - start)
```

#### Step 4: Simplify the Example

- Set `n = 500` (sleep for 0.5 seconds) to make the sleep shorter and easier to test.
- Run the code and observe the output to confirm the elapsed time is around 0.5 seconds.

---

### Why This Is in the Course

- **Debugging Skills**: Timing is a key debugging technique. It helps you identify slow parts of your code, verify behavior, and optimize performance.
- **Practical Tool**: `time.time()` is a simple way to measure elapsed time, and this example shows how to use it.
- **Foundation for Profiling**: This leads to more advanced tools like Python’s `timeit` module or profilers (e.g., `cProfile`), which the lecture might cover next.

---

### Takeaway

- **Core Concept**: Timing measures how long code takes to run, helping you debug performance issues, verify behavior, and optimize.
- **How It Helps Debugging**:
  - Confirms operations (like `time.sleep`) work as expected.
  - Identifies slow code sections.
  - Lets you compare different implementations.
- **Tracing Tips**:
  - Use a table to track variables (`n`, `start`, elapsed time).
  - Add print statements to see values at each step.
  - Simplify the example (e.g., smaller `n`) to make tracing easier.

Try running the code with `n = 2000` and see if the elapsed time is close to 2 seconds. Want to trace another example together?

---

import time
import logging

---

real time , system time `command time`, user level code, kernel level code

- time curl http
  user time -> your command time

# Profiling (how to optimize the code)

two types

- tracing profiler
- sampling profiler

![](20250405-cs-missing-semester/2025-04-05-03-45-00.png)

Let’s dive into this slide from your MIT course lecture, which introduces the concept of profiling in Python using the `cProfile` module. The teacher is teaching you how to use a profiler to analyze the performance of your code, specifically to identify where time is being spent. The command shown in the slide uses `cProfile` to profile a script called `grep.py`, and the slide mentions "match like the the grep arguments here," indicating a focus on understanding how to profile code with specific arguments. I’ll break down the core concept of profiling, explain the command, and help you understand how this fits into debugging and performance optimization, especially since you’ve been exploring timing and logging in earlier sections.

---

### Core Concept: Profiling with `cProfile`

#### What Is Profiling?

Profiling is a technique to measure the performance of your code by analyzing how much time (and sometimes memory) different parts of your program consume. It helps you identify bottlenecks—parts of the code that are slow and might need optimization.

- **Why Profile?**

  - Instead of guessing where your code is slow, a profiler gives you data: Which functions are called the most? Which ones take the most time?
  - This builds on the timing concept you learned earlier (`time.time()` in `timing.py`), but profiling provides a more detailed breakdown.

- **How Does `cProfile` Work?**
  - `cProfile` is a built-in Python module that tracks every function call in your program, recording:
    - **Number of Calls (`ncalls`)**: How many times a function is called.
    - **Total Time (`tottime`)**: Total time spent in the function, excluding calls to other functions.
    - **Cumulative Time (`cumtime`)**: Total time spent in the function, including calls to other functions.
  - It generates a report showing this data for each function, helping you pinpoint performance issues.

#### First Principles: Why Is This Useful?

Imagine you’re cooking a meal, and it takes too long. You could time the entire process (like in `timing.py`), but that only tells you the total time (e.g., 30 minutes). Profiling is like timing each step (chopping, boiling, baking) to see which one is the slowest. If baking takes 20 minutes, you might decide to optimize that step (e.g., use a better oven). In programming, profiling helps you find the “baking” in your code—the slow functions—so you can optimize them.

---

### The Command Explained

The slide shows this command being executed:

```bash
~/p/m/deb >>> python -m cProfile -s tottime grep.py 1000 '^import[ \t].*[skdef][ \t].*'
```

Let’s break it down:

#### 1. **Command Structure**

- **`python`**: Runs the Python interpreter.
- **`-m cProfile`**: Runs the `cProfile` module as a script, which profiles the program you specify.
- **`-s tottime`**: Sorts the profiling output by `tottime` (total time spent in each function, excluding sub-calls). Other sorting options include `cumtime` (cumulative time), `ncalls` (number of calls), etc.
- **`grep.py`**: The Python script to profile. Presumably, this is a script that searches for patterns in text (like the Unix `grep` command).
- **`1000`**: The first argument to `grep.py`, likely the number of lines to process or iterations to run.
- **`'^import[ \t].*[skdef][ \t].*'`**: The second argument to `grep.py`, a regular expression pattern to match. Let’s break down the pattern:
  - `^import`: Matches lines starting with "import".
  - `[ \t]`: Matches a space or tab.
  - `.*`: Matches any characters (zero or more).
  - `[skdef]`: Matches one character that is either `s`, `k`, `d`, `e`, or `f`.
  - `[ \t]`: Another space or tab.
  - `.*`: More characters.
  - **Meaning**: This pattern matches lines like `import sys`, `import mathdef`, or `import sk`, but the `[skdef]` part is a bit odd—it might be a typo or a specific test case (e.g., meant to match certain import statements).

#### 2. **What `grep.py` Might Look Like**

The slide doesn’t show `grep.py`, but based on the context, it’s likely a script that searches for lines matching a pattern. Here’s a possible implementation:

```python
import sys
import re

def grep(pattern, lines):
    regex = re.compile(pattern)
    for line in lines:
        if regex.search(line):
            print(line.strip())

if __name__ == "__main__":
    num_lines = int(sys.argv[1])  # e.g., 1000
    pattern = sys.argv[2]  # e.g., '^import[ \t].*[skdef][ \t].*'
    # Simulate reading lines (e.g., from a file or generated)
    lines = ["import sys\n", "print('hello')\n", "import mathdef\n"] * (num_lines // 3)
    grep(pattern, lines)
```

- This script takes a number of lines (`1000`) and a pattern, then searches for matches in a simulated list of lines.

#### 3. **What the Command Does**

- **Profiles `grep.py`**: `cProfile` tracks every function call in `grep.py` while it processes 1000 lines with the given pattern.
- **Sorts by `tottime`**: The output will show functions sorted by the time they spend executing (excluding time spent in sub-functions).
- **Expected Output**: A table like this:
  ```
     ncalls  tottime  percall  cumtime  percall filename:lineno(function)
        1000    0.050    0.000    0.060    0.000 grep.py:4(grep)
        3000    0.030    0.000    0.040    0.000 {method 'search' of 're.Pattern'}
         ...
  ```
  - `grep`: The main function, taking 0.050 seconds of `tottime`.
  - `re.search`: Called 3000 times (once per line), taking 0.030 seconds.

---

### Core Concept: How Profiling Helps

The teacher is teaching you how to use `cProfile` to debug performance issues, building on the timing concepts from `timing.py`. Here’s how profiling helps:

#### 1. **Identifies Bottlenecks**

- The `grep.py` script might be slow because:
  - The regular expression matching (`re.search`) is inefficient.
  - The loop over 1000 lines is taking too long.
- `cProfile` shows you exactly which functions are slow. If `re.search` takes 90% of the time, you know to optimize the regex or use a different approach (e.g., string methods like `startswith`).

#### 2. **Understands Function Call Overhead**

- Profiling shows how many times each function is called (`ncalls`).
- Example: If `re.search` is called 3000 times, you might realize you can compile the regex once outside the loop (using `re.compile`) to save time.

#### 3. **Compares Total vs. Cumulative Time**

- `tottime`: Time spent in the function itself.
- `cumtime`: Time including sub-calls.
- If `grep` has a high `cumtime` but low `tottime`, the slowness is in functions it calls (e.g., `re.search`). This helps you drill down to the root cause.

#### 4. **Matches Arguments for Testing**

- The slide mentions “match like the the grep arguments here.” The teacher is emphasizing that profiling should be done with realistic inputs (e.g., the pattern `^import[ \t].*[skdef][ \t].*` and 1000 lines).
- Why? Performance depends on the input. A simple pattern like `hello` might be fast, but a complex regex like this one might reveal bottlenecks (e.g., backtracking in the regex engine).

#### 5. **Improves Debugging Workflow**

- In your earlier lectures, you learned:
  - **Timing** (`timing.py`): Measures total time for a block of code.
  - **Logging**: Tracks events and errors.
- Profiling with `cProfile` adds a new tool: It breaks down the time into per-function contributions, giving you a detailed view of performance.

---

### How This Fits with PyPy Discussion

In your previous question, you asked about PyPy’s disadvantages. This slide ties in because `cProfile` is designed for CPython, and its results can be misleading on PyPy due to PyPy’s JIT compilation. Here’s why:

- **PyPy Issue**: `cProfile` adds overhead by tracking every function call, which can confuse PyPy’s JIT. The profiling data might not accurately reflect PyPy’s performance (e.g., it might show inflated times for JIT-compiled code).
- **What to Beware Of**: If you try to profile `grep.py` with PyPy, the results might not be reliable. PyPy recommends using its own profiling tools like `vmprof` instead.
- **Relevance to Lecture**: The teacher is likely using CPython for this demo (since `cProfile` works best there), showing you how to profile in a standard Python environment.

---

### Tips for Tracing Variables in This Context

Since you mentioned tracing variables like `n` was hard, let’s trace the profiling process conceptually (since `grep.py` isn’t fully shown):

#### 1. **Understand the Variables**

- **Command Arguments**:
  - `sys.argv[1] = "1000"`: Number of lines.
  - `sys.argv[2] = "^import[ \t].*[skdef][ \t].*"`: Pattern.
- **Inside `grep.py`**:
  - `num_lines`: Converted from `sys.argv[1]`.
  - `pattern`: The regex pattern.
  - `lines`: List of lines to search.

#### 2. **Trace with a Table**

Let’s trace a simplified run of `grep.py` with 3 lines instead of 1000:

| Step         | `num_lines` | `pattern`                      | `lines`                                                    | Function Call          | Action                     |
| ------------ | ----------- | ------------------------------ | ---------------------------------------------------------- | ---------------------- | -------------------------- |
| Start        | 3           | `^import[ \t].*[skdef][ \t].*` | -                                                          | -                      | Parse `sys.argv`           |
| Create Lines | 3           | `^import[ \t].*[skdef][ \t].*` | `["import sys\n", "print('hello')\n", "import mathdef\n"]` | -                      | Generate lines             |
| Call `grep`  | 3           | `^import[ \t].*[skdef][ \t].*` | `["import sys\n", ...]`                                    | `grep(pattern, lines)` | Compile regex, loop starts |
| Line 1       | -           | -                              | `import sys\n`                                             | `regex.search(line)`   | Matches → Print            |
| Line 2       | -           | -                              | `print('hello')\n`                                         | `regex.search(line)`   | No match                   |
| Line 3       | -           | -                              | `import mathdef\n`                                         | `regex.search(line)`   | Matches → Print            |

- **Profiling Output** (hypothetical):
  ```
     ncalls  tottime  percall  cumtime  percall filename:lineno(function)
          1    0.001    0.001    0.003    0.003 grep.py:4(grep)
          3    0.002    0.001    0.002    0.001 {method 'search' of 're.Pattern'}
  ```

#### 3. **Simplify the Example**

- Run `grep.py` with a smaller number of lines (e.g., 10) to make the profiling output shorter and easier to analyze.
- Use a simpler pattern (e.g., `^import`) to reduce regex complexity.

#### 4. **Add Print Statements**

Inside `grep.py`, add prints to see what’s happening:

```python
def grep(pattern, lines):
    regex = re.compile(pattern)
    print(f"Compiled pattern: {pattern}")
    for i, line in enumerate(lines):
        print(f"Checking line {i}: {line.strip()}")
        if regex.search(line):
            print(f"Match found: {line.strip()}")
            print(line.strip())
```

---

### Why This Is in the Course

- **Profiling as a Debugging Tool**: Builds on timing (`timing.py`) and logging. Timing gives you the total time; profiling breaks it down by function.
- **Practical Skill**: In real projects, you’ll need to optimize code. Profiling helps you find bottlenecks systematically.
- **Specific Example**: The `grep.py` script with a regex pattern shows how profiling applies to a realistic task (text searching), emphasizing the importance of testing with real inputs.

---

### Takeaway

- **Core Concept**: Profiling with `cProfile` analyzes your code’s performance, showing where time is spent (e.g., in `grep` or `re.search`).
- **How It Helps**: Identifies bottlenecks, measures function call overhead, and ensures you’re testing with realistic inputs (like the regex pattern).
- **Command Breakdown**:
  - `python -m cProfile -s tottime grep.py 1000 '^import[ \t].*[skdef][ \t].*'`
  - Profiles `grep.py`, sorts by `tottime`, with arguments `1000` (lines) and a regex pattern.
- **Tie to PyPy**: `cProfile` is best for CPython; PyPy needs tools like `vmprof` for accurate profiling.

Try running `cProfile` on a simple script (e.g., your logging code from earlier) to see where time is spent. Want to profile a specific example together?

python xx | tac -> show the command on the bottom (like a less)

---

now this is the line profiler
[pyutils/line_profiler: Line-by-line profiling for Python](https://github.com/pyutils/line_profiler)

@profile

memory profiler , cpu profiler etc

sudo perf record stress(command or procss name) -c 1

perf -g -> graph
flame graph

- [brendangregg/FlameGraph: Stack trace visualizer](https://github.com/brendangregg/FlameGraph)

python -> call graph

[Lewiscowles1986/py-call-graph: pycallgraph is a Python module that creates call graphs for Python programs.](https://github.com/Lewiscowles1986/py-call-graph)

- perf seem much better as system-wide
- htop

python -m http.server 4444
sudo lsof | grep ":4444 .LISTEN"

hyprfine test to command

## iotop for I/O in linux

source: https://missing-semester-cn.github.io/2020/debugging-profiling/

---

- **通用监控** - 最流行的工具要数 [`htop`](https://htop.dev/), 了，它是 [`top`](http://man7.org/linux/man-pages/man1/top.1.html) 的改进版。`htop` 可以显示当前运行进程的多种统计信息。`htop` 有很多选项和快捷键，常见的有：`<F6>` 进程排序、 `t` 显示树状结构和 `h` 打开或折叠线程。 还可以留意一下 [`glances`](https://nicolargo.github.io/glances/) ，它的实现类似但是用户界面更好。如果需要合并测量全部的进程， [`dstat`](http://dag.wiee.rs/home-made/dstat/) 是也是一个非常好用的工具，它可以实时地计算不同子系统资源的度量数据，例如 I/O、网络、 CPU 利用率、上下文切换等等；
- **I/O 操作** - [`iotop`](http://man7.org/linux/man-pages/man8/iotop.8.html) 可以显示实时 I/O 占用信息而且可以非常方便地检查某个进程是否正在执行大量的磁盘读写操作；
- **磁盘使用** - [`df`](http://man7.org/linux/man-pages/man1/df.1.html) 可以显示每个分区的信息，而 [`du`](http://man7.org/linux/man-pages/man1/du.1.html) 则可以显示当前目录下每个文件的磁盘使用情况（ **d** isk **u** sage）。`-h` 选项可以使命令以对人类（**h** uman）更加友好的格式显示数据；[`ncdu`](https://dev.yorhel.nl/ncdu) 是一个交互性更好的 `du` ，它可以让您在不同目录下导航、删除文件和文件夹；
- **内存使用** - [`free`](http://man7.org/linux/man-pages/man1/free.1.html) 可以显示系统当前空闲的内存。内存也可以使用 `htop` 这样的工具来显示；
- **打开文件** - [`lsof`](http://man7.org/linux/man-pages/man8/lsof.8.html) 可以列出被进程打开的文件信息。 当我们需要查看某个文件是被哪个进程打开的时候，这个命令非常有用；
- **网络连接和配置** - [`ss`](http://man7.org/linux/man-pages/man8/ss.8.html) 能帮助我们监控网络包的收发情况以及网络接口的显示信息。`ss` 常见的一个使用场景是找到端口被进程占用的信息。如果要显示路由、网络设备和接口信息，您可以使用 [`ip`](http://man7.org/linux/man-pages/man8/ip.8.html) 命令。注意，`netstat` 和 `ifconfig` 这两个命令已经被前面那些工具所代替了。
- **网络使用** - [`nethogs`](https://github.com/raboof/nethogs) 和 [`iftop`](http://www.ex-parrot.com/pdw/iftop/) 是非常好的用于对网络占用进行监控的交互式命令行工具。

---

- vendoringe

---

# Metaprogramming 2025-04-05

- build system
  using xxx you want to build who need this dependence
  dependence -> A dependence , in order for A, need to B
  sequences of command to get another

- make(not great for complex project, but good for small one)
