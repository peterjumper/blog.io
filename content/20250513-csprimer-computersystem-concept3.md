---
id: 20250513-csprimer-computersystem-concept3
aliases:
  - csprimer-computersystem-concept3
tags: []
---

# csprimer-computersystem-concept3

[NASM Tutorial](https://cs.lmu.edu/~ray/notes/nasmtutorial/)
[hackclub/some-assembly-required: 📖 An approachable introduction to Assembly.](https://github.com/hackclub/some-assembly-required?tab=readme-ov-file)
![](20250513-csprimer-computersystem-concept3/2025-05-13-02-02-15.png)

- there is two common x64 , inter and att (linux prefer)
  push -> pushq -> push to queue

att:
movq , movb (b for byte), bl -> long byte

movq , q for qute word quart word -> 64 bit -> quart of 64 , 16

- subq:
  substracting 16 from %rsp

- operator order is difference btw att and intel

- look at the construction

one text section , loaded in the memory

---

# Programming C

learn x in y minutes
[C, Go - Hyperpolyglot](https://hyperpolyglot.org/c)
read c code , linux source code

- high level of struct
- compile , c knowledge with machine

hello world in c :

int main() {} -> why int a linux culture -> 0 mean successful like
work && run bash order

if return 1; -> not , it will not run as successful, can && after

return -1 -> assertion fail -> fail reminder in terminal

int bitcount(int n) {
int count = 0;
while (n){

}
}

in c , 0 mean true , 1 -> false

- don't have boolean in c , so using `while(n)-> keep runing while n is not 0 `

`n & 0x01` is a **bitwise AND** operation that checks whether the **least significant bit (LSB)** of `n` is `1` or `0`.

### Explanation:

- `0x01` is hexadecimal for `00000001` in binary.
- `n & 0x01` compares `n` with `00000001` using bitwise AND:

  - If the LSB of `n` is `1`, the result is `1`.
  - If the LSB is `0`, the result is `0`.

### Example:

```cpp
n = 5;          // binary: 0101
n & 0x01 = 1    // because the LSB is 1
```

This is commonly used to count the number of `1`s in a binary number (also known as the Hamming weight or population count).

---

**Also, your function is missing a return statement.** Here's the corrected version:

```cpp
int bitcount(int n) {
  int count = 0;
  while (n) {
    if (n & 0x01) {
      count += 1;
    }
    n >>= 1;
  }
  return count;
}
```

Let me know if you want a version that’s more efficient.

as there is only 1 and 0 out there , so if there is 1 in the lsb , least significant bit -> shift right until 0

![](20250513-csprimer-computersystem-concept3/2025-05-13-02-50-45.png)

int bitcount(int n) {
int count = 0;
while (n) {
count += n & 0x01;
n >>= 1;
}
return count;
}

- refactor
  as 0 dont affect count, add them all in here lol

  ```c
  int main() {
  assert(bitcount(0) == 0);
  assert(bitcount(1) == 1);
  assert(bitcount(3) == 2);
  assert(bitcount(8) == 1);
  // harder case:
  assert(bitcount(0xffffffff) == 32);
  printf("OK\n");
  }

  ```

assert(bitcount(0xffffffff) == 32); this break the while(n) loop , so the n != 0 for 0xffffffff

---

### 🔢 What is `0xffffffff`?

In binary, `0xffffffff` is:

```
11111111 11111111 11111111 11111111  // 32 bits
```

That’s **all bits set to 1** — which equals `4294967295` in **unsigned** interpretation.

---

### 🧠 Signed vs Unsigned Int in C

- `int` is **signed** (can represent negative and positive numbers).
- It uses **two's complement** representation to handle negatives.

---

### ⚙️ Two's Complement Concept

In **two's complement**, the **highest bit (leftmost bit)** is the **sign bit**:

- `0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx` → positive
- `1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx` → negative

To get the negative value of a binary number:

1. Invert all the bits
2. Add 1

So in 32-bit signed `int`:

- `0x00000001` → 1
- `0x7fffffff` → 2,147,483,647 (max signed int)
- `0x80000000` → -2,147,483,648 (min signed int)
- `0xffffffff` → **-1**

---

### ✅ Why `0xffffffff` = -1 in signed int

Let’s apply two’s complement:

- `0xffffffff` = `11111111 11111111 11111111 11111111`
- Invert: `00000000 00000000 00000000 00000000`
- Add 1: `00000000 00000000 00000000 00000001` → that's `1`
- So original = `-1`

Hence, `0xffffffff` is interpreted as **-1** in a signed `int`.

---

### 🚫 Why the Loop Breaks

Right-shifting signed -1:

- `-1 >> 1` → still `-1`, because the sign bit (`1`) is preserved.
- So `n` never becomes `0`, and `while (n)` becomes **infinite loop**.

---

### Summary

| Hex          | Binary (32-bit)                       | Interpreted as              |
| ------------ | ------------------------------------- | --------------------------- |
| `0xffffffff` | `11111111 11111111 11111111 11111111` | `-1` (signed int)           |
|              |                                       | `4294967295` (unsigned int) |

So: **same bits, different meaning depending on signed vs unsigned.**

Let me know if you'd like a visual to reinforce this!

---

int bitcount(unsigned n) {
int count = 0;
while (n) {
count += n & 0x01;
n >>= 1;
}
return count;
}

int n -> unsigned -> fixed

![](20250513-csprimer-computersystem-concept3/2025-05-13-03-08-11.png)

---

before using belew , it loop 32 times for case 0xfff ... == 32

- x & x-1 -> deleted the rightmost bit of x _using bitwise &_

![](20250513-csprimer-computersystem-concept3/2025-05-13-03-11-10.png)
Excellent question — this is a classic bit manipulation trick often called **Brian Kernighan’s Algorithm**.

---

### 🔍 What does it do?

This line:

```c
n &= (n - 1);
```

**clears the lowest set bit** (the rightmost `1`) in `n`.

Each time this happens, we increment `count`.

So instead of looping through **all 32 bits**, we loop only through the **number of set bits**.

---

### 🔥 Why is it faster?

Let’s compare with your previous method:

#### Previous method:

```c
while (n) {
  count += n & 1;
  n >>= 1;
}
```

- Always does **up to 32 iterations**, checking each bit one-by-one.

#### New method:

```c
while (n) {
  n &= (n - 1);
  count++;
}
```

- Does **only as many iterations as there are 1s** in `n`.

---

### 🧠 Example: `n = 0b10110000`

Set bits: 3
Old loop → 8 iterations
New loop → 3 iterations ✔️

---

### 💡 Why `n & (n - 1)` clears the lowest set bit?

Let’s take an example:

```
n       =  0b10110000
n - 1   =  0b10101111
---------------------
n & (n-1)= 0b10100000   ← rightmost 1 cleared
```

So each iteration **removes one 1**, getting us closer to `0` faster.

---

### Summary:

| Method       | Iterations Needed              | Performance Benefit    |
| ------------ | ------------------------------ | ---------------------- |
| `n >>= 1`    | Up to 32                       | Slower for sparse bits |
| `n &= (n-1)` | Only set bits (Hamming weight) | Faster overall         |

Your teacher’s version is **more efficient**, especially when `n` has **few set bits**. It's a smart use of bitwise logic.

---

advanced C :
compiler ->

pop count (compiler) population count

cc -O3 -fomit-frame-pointer -march=native -c bitcount.c

objdump -d bitcount.o

---

### 🧠 What is `popcnt`?

- `popcnt` is a **CPU instruction** that counts the number of `1` bits (set bits) in a binary number.
- It's built into modern CPUs (like Intel and AMD).
- It’s extremely fast — much faster than any loop.

> Think of it as a "hardware-accelerated bitcount."

---

### ✅ Why your teacher used `-march=native` and `-O3`

- `-O3`: Tells the compiler to **fully optimize** the code.
- `-march=native`: Allows the compiler to use **CPU-specific features**, like `popcnt`.

So when the compiler sees your function:

```c
int bitcount(unsigned n) {
  int count = 0;
  while (n) {
    n &= (n-1);
    count++;
  }
  return count;
}
```

Instead of compiling a loop, it says:

> “Oh! This is just a popcount — I’ll replace it with the **`popcnt`** instruction.”

---

### 🧩 What does the assembly mean?

```
0: 31 c0           xor    %eax, %eax       // set EAX = 0 (clear return value register)
2: f3 0f b8 c7     popcnt %edi, %eax       // EAX = popcount(EDI)
6: c3              ret                     // return
```

Let’s break it down:

| Assembly            | Meaning                                     |
| ------------------- | ------------------------------------------- |
| `xor %eax, %eax`    | Clear the `eax` register (set to 0)         |
| `popcnt %edi, %eax` | Count bits in `edi` and put result in `eax` |
| `ret`               | Return from function                        |

**Registers:**

- `%edi`: where the first argument (`unsigned n`) is passed (in 64-bit calling convention).
- `%eax`: where the return value is stored.

---

### 🚀 Summary

- The compiler **recognized** your bitcount function and replaced it with a single fast `popcnt` CPU instruction.
- This is only possible with **optimization flags** (`-O3 -march=native`) and on CPUs that support `popcnt`.

So this is your teacher showing you:

> _"Writing clever code is cool, but modern compilers and CPUs can do even better!"_

Let me know if you want a visual of how registers or `popcnt` work internally.

---

adding inline compiler wtf

`#include <nmintrin.h>`

\_\_builtin_popcount(n) Counts 1-bits efficiently
<nmmintrin.h> Enables SSE4.2 intrinsics like popcnt
Replaces manual loop Cleaner, faster, compiler-optimized

- using mechine code instruction -> more optimize

as it is usign mechine instruction , not all computer have popcount , so if compile didn't set to march = native , it
will just use other assembly way

no loop in in the assembly

primer suggesting this book:

> Hacker's Delight

[[20250513-777-csbooks-hackers-delight|777-csbooks-hackers-delight]]

there is counting tips about bitw

Parallel way to count the bit from pair

32 -> 16 -> 4 -> 2
pair 2 bit and sum

I am not gpt genthis right in below

Ah! If your teacher mentioned that the algorithm allows you to "run in **parallel**," then he’s likely referring to an approach inspired by **SIMD-style** or **parallel prefix sum** techniques.

---

## 🧠 The Core Idea: Parallel Byte Aggregation

When decoding a multi-byte little-endian number (e.g. `a4 01 00 00`), the normal method is **sequential**:

```python
value = b[0] + (b[1] << 8) + (b[2] << 16) + (b[3] << 24)
```

This is inherently sequential because each shift depends on the byte's position.

But with **parallel processing**, you can:

- Split the bytes into **groups (e.g. 2-byte chunks)**
- Perform operations on those chunks **in parallel**
- Combine the partial results later

---

## ⚡ Example: Parallel 16-bit Pairing

Let’s say you have 4 bytes:

```
bs = [a4, 01, 00, 00]
```

Instead of:

```python
a4 + 01 << 8 + 00 << 16 + 00 << 24
```

You could do:

1. Group into 2-byte chunks:

   ```
   chunk1 = a4 01  => little-endian: 0x01a4
   chunk2 = 00 00  => 0x0000
   ```

2. Then compute:

   ```python
   value = chunk1 + (chunk2 << 16)
   ```

You’re now doing **fewer additions**, and this structure can be **parallelized** in low-level or SIMD hardware (e.g., SSE/AVX).

---

## 🚀 In SIMD Hardware:

On CPUs that support SIMD (like Intel with AVX), operations like "multiply and accumulate" or "shift and add" on multiple 16- or 32-bit integers **can be vectorized**, meaning done in **parallel registers**.

Even in GPU programming (CUDA, OpenCL), this matters.

---

## 🧪 Summary:

Your teacher is hinting at an **algorithm that makes endian conversion more parallel-friendly**:

| Feature                            | Explanation                             |
| ---------------------------------- | --------------------------------------- |
| ✅ Break into 2-byte chunks        | Reduces loop iterations                 |
| ✅ SIMD-friendly                   | You can shift/add in **parallel lanes** |
| ✅ More efficient for large arrays | Works well in image or video data       |
| ✅ CPU/GPU optimization            | Used in compilers and video codecs      |

---

## 🧰 Python can't _truly_ do this in parallel, but...

You could simulate the logic and understand how it reduces dependency per byte.

Want me to show you this idea with an example that compares **standard vs 2-byte parallel-style** summing in Python?

---

Ah! You’re thinking of **Divide and Conquer** algorithms. (That's the correct spelling 😊)

---

### 🧠 What Is a Divide and Conquer Algorithm?

**Divide and Conquer** is a strategy to solve complex problems by:

1. **Divide** — Breaking the problem into smaller subproblems.
2. **Conquer** — Solving each subproblem **recursively** (or in parallel).
3. **Combine** — Merging the solutions of subproblems to get the final answer.

---

### ✅ Classic Examples

| Problem                              | How Divide & Conquer Works                                                   |
| ------------------------------------ | ---------------------------------------------------------------------------- |
| **Merge Sort**                       | Divide the array, sort both halves recursively, then merge the sorted halves |
| **Quick Sort**                       | Partition the array, then sort left and right parts recursively              |
| **Binary Search**                    | Divide search space in half each time                                        |
| **Fast Fourier Transform (FFT)**     | Split signals, apply FFT recursively, then combine frequency results         |
| **Matrix Multiplication (Strassen)** | Break matrix into quadrants, multiply submatrices recursively                |

---

### 🧮 For Byte Summing?

Yes — your teacher might be suggesting a **Divide and Conquer approach to summing bytes**, like:

- Pair 2 bytes together and form small integers
- Sum pairs recursively
- Combine results

This lets you **parallelize** the summing, especially if:

- You're reading huge binary files
- You're processing pixels or data blocks
- You're optimizing for SIMD/CPU threads

---

### 👇 In simple Python example:

```python
def le_dc(bs):  # Divide and Conquer for little-endian bytes
    if len(bs) == 1:
        return bs[0]
    mid = len(bs) // 2
    left = le_dc(bs[:mid])
    right = le_dc(bs[mid:])
    return left + (right << (8 * mid))
```

Same result as the loop-based method, but this can be done **in parallel** in theory, because `left` and `right` are independent until the final shift + add.

---

Would you like a visual animation or simple diagram of how this divide-and-conquer version works compared to normal summing?

- primer mention :
  What Is a Divide and Conquer Algorithm?

Divide and Conquer is a strategy to solve complex problems by:

Divide — Breaking the problem into smaller subproblems.

Conquer — Solving each subproblem recursively (or in parallel).

Combine — Merging the solutions of subproblems to get the final answer.

---
