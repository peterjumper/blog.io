---
id: 20250313-777-tricks-logic-programming
aliases:
  - 777-tricks-logic-programming
tags: []
---

# 777-tricks-logic-programming

It seems like you're referencing some logical mechanics (like De Morgan's laws) and asking for "useful mechanic skips and tricks." I’ll assume you're looking for practical tips or shortcuts, possibly related to logic, programming, or problem-solving, given the example you provided. If you meant something else (like video game mechanics or a specific domain), feel free to clarify!

Here are some **useful tricks and shortcuts** based on the logic you mentioned and beyond:

---

### 1. Logic Simplification with De Morgan’s Laws

Your example `(NOT(X OR Y)) == (NOT(X) AND NOT(Y))` is a classic application of De Morgan’s laws. These are super useful for simplifying conditions in programming, circuits, or math:

- **Trick 1: Reverse OR to AND (and vice versa)**

  - `(NOT(X OR Y)) = (NOT(X) AND NOT(Y))`
  - `(NOT(X AND Y)) = (NOT(X) OR NOT(Y))`
  - **Use case**: When debugging or optimizing code, flip the logic to make it more readable or efficient.  
    _Example_: Instead of `if (!(a || b))`, write `if (!a && !b)`.

- **Skip**: Avoid nested negations by applying this directly—saves mental effort and reduces errors.

---

### 2. Programming Shortcut: Toggle with XOR

- **Trick**: Use the XOR operator (`^`) to flip values without an if-statement.
  - `x ^= 1` toggles `x` between 0 and 1 (in binary contexts).
  - **Why it works**: XOR with 1 flips a bit; XOR with itself cancels out.
  - **Use case**: Toggling a boolean or bit flag in one line.  
    _Example_: `lightOn ^= true;` switches a light on/off.

---

### 3. Math Trick: Fast Power of 2 Check

- **Trick**: To check if a number `n` is a power of 2, use `n & (n - 1) == 0`.
  - **Why it works**: Powers of 2 have exactly one 1-bit (e.g., 2 = 0010, 4 = 0100), and subtracting 1 flips all bits after that 1 to 1s (e.g., 4-1 = 0011). ANDing them gives 0.
  - **Skip**: No need for loops or division—super fast for bit-level checks.

---

### 4. Search Optimization: Binary Search Skip

- **Trick**: When searching sorted data, don’t scan linearly—jump halves with binary search.
  - Instead of checking every element (O(n)), cut the search space in half each step (O(log n)).
  - **Use case**: Finding an element in a sorted list or array.
  - **Skip**: Avoid writing loops for small datasets by guessing midpoints manually if you’re just prototyping.

---

### 5. String Reversal Hack

- **Trick**: Reverse a string in-place with two pointers (start and end), swapping as you go.
  - _Example (Python)_: `s = list("hello"); l, r = 0, len(s)-1; while l < r: s[l], s[r] = s[r], s[l]; l += 1; r -= 1`
  - **Skip**: No need for extra memory or built-in reverse functions—saves space and time.

---

### 6. Quick Parity Check

- **Trick**: Use `n & 1` to check if a number is odd or even.
  - If result is 1, it’s odd; if 0, it’s even.
  - **Why it works**: The least significant bit is 1 for odd numbers, 0 for even.
  - **Skip**: Avoid modulo (`% 2`) for a faster bitwise operation.

---

### 7. Everyday Problem-Solving: Work Backwards

- **Trick**: For puzzles or planning, start from the goal and reverse-engineer the steps.
  - _Example_: Need to solve a maze? Start at the exit and trace back to the start.
  - **Skip**: Avoid trial-and-error by focusing on what must be true at the end.

---

If you had a specific domain in mind (like coding, gaming, or hardware), let me know, and I can tailor more tricks for you! What do you think—any of these useful for what you’re working on?

Glad you found those useful! Here’s another batch of **tricks and skips** across different domains—logic, programming, math, and general problem-solving. I’ll keep them practical and concise:

---

### 8. Bitwise Multiplication/Division by Powers of 2

- **Trick**: Use bit shifts to multiply or divide by powers of 2.
  - Left shift (`<<`) multiplies: `n << 1` = `n * 2`, `n << 2` = `n * 4`.
  - Right shift (`>>`) divides: `n >> 1` = `n / 2`, `n >> 2` = `n / 4` (integer division).
  - **Why it works**: Shifting bits adjusts the binary place values.
  - **Skip**: Avoid slower multiplication/division operations in performance-critical code.  
    _Example_: `x = 5 << 3` gives `40` (5 \* 8).

---

### 9. Fast Loop Exit with Flags

- **Trick**: Use a boolean flag to break out of nested loops in one go.
  - Instead of multiple `break` statements, set `done = true` and check it.
  - _Example (Python)_:
    ```python
    done = False
    for i in range(10):
        for j in range(10):
            if some_condition(i, j):
                done = True
                break
        if done:
            break
    ```
  - **Skip**: Avoid messy control flow or extra conditions in each loop.

---

### 10. Math Trick: Sum of Consecutive Integers

- **Trick**: Sum numbers from 1 to `n` with `n * (n + 1) / 2`.
  - _Example_: 1 + 2 + 3 + 4 + 5 = `5 * 6 / 2 = 15`.
  - **Why it works**: Pairs from opposite ends (1+n, 2+(n-1)) average to `(n+1)`, and there are `n/2` pairs.
  - **Skip**: No need to loop or manually add—great for quick mental math or coding.

---

### 11. String Comparison: Early Exit

- **Trick**: When comparing two strings, check lengths first.
  - If `len(str1) != len(str2)`, they can’t be equal—skip the full comparison.
  - **Use case**: Speeds up equality checks in large datasets.
  - **Skip**: Avoid character-by-character comparison when it’s unnecessary.

---

### 12. Memoization for Recursion

- **Trick**: Cache results of expensive recursive calls to avoid recomputation.
  - _Example (Fibonacci in Python)_:
    ```python
    memo = {}
    def fib(n):
        if n in memo: return memo[n]
        if n <= 1: return n
        memo[n] = fib(n-1) + fib(n-2)
        return memo[n]
    ```
  - **Skip**: Cuts time from exponential (O(2^n)) to linear (O(n)) by reusing results.

---

### 13. Probability Shortcut: Complementary Events

- **Trick**: Calculate the chance something _doesn’t_ happen, then subtract from 1.
  - _Example_: Probability of rolling at least one 6 in 3 dice rolls?
    - P(no 6s) = (5/6)^3 = 125/216.
    - P(at least one 6) = 1 - 125/216 = 91/216.
  - **Skip**: Avoid listing all success cases—simpler and faster.

---

### 14. Array Trick: Two-Pointer Technique

- **Trick**: Use two pointers to solve problems like finding pairs or reversing.
  - _Example (Find pair summing to target)_:
    ```python
    nums = [2, 7, 11, 15]; target = 9
    left, right = 0, len(nums)-1
    while left < right:
        if nums[left] + nums[right] == target:
            print(left, right)
            break
        elif nums[left] + nums[right] < target:
            left += 1
        else:
            right -= 1
    ```
  - **Skip**: Avoid nested loops (O(n^2))—this is O(n) with a sorted array.

---

### 15. Everyday Hack: Binary Decision Elimination

- **Trick**: When choosing between options, eliminate half at each step.
  - _Example_: Picking a restaurant from 8 choices?
    - Step 1: Italian or not? (4 left)
    - Step 2: Cheap or fancy? (2 left)
    - Step 3: Near or far? (1 left)
  - **Skip**: Avoid overthinking every option—cuts decision fatigue.

---

### 16. Code Debugging: Print Halfway

- **Trick**: When a program fails, add a print statement halfway through to narrow the bug’s location.
  - If it prints, the issue’s in the second half; if not, it’s in the first. Repeat.
  - **Skip**: Don’t comb through every line—divide and conquer like binary search.

---

How’s that? These span a mix of technical and practical shortcuts. Want more in a specific area (e.g., coding, math, or something else)? Let me know!
