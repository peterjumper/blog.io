---
id: 1738895060-difference-of-squares-in-c
aliases:
  - Difference of Squares in C
tags: []
---

# Difference of Squares in C

```markdown name=explanation.md
# Explanation of the Difference of Squares Formulas

This document explains the mathematical formulas used in the C code for calculating the difference of squares, using GitHub-flavored Markdown with embedded math code blocks.

## 1. Sum of the Squares

The sum of the squares of the first *n* natural numbers is given by:

```math
1^2 + 2^2 + 3^2 + \ldots + n^2 = \frac{n(n+1)(2n+1)}{6}
```

### Derivation Outline

1. **Polynomial Form Assumption**

   Assume the sum \(S(n)\) can be expressed as a cubic polynomial:
   
   ```math
   S(n) = an^3 + bn^2 + cn + d
   ```
   
   Since \( S(0) = 0 \) (the sum of zero numbers is 0), it follows that:
   
   ```math
   d = 0
   ```

2. **Determining the Coefficients**

   Plug in small values for \( n \):
   
   - For \( n = 1 \):
     
     ```math
     S(1) = a(1)^3 + b(1)^2 + c(1) = a + b + c = 1
     ```
   
   - For \( n = 2 \):
     
     ```math
     S(2) = 8a + 4b + 2c = 1^2 + 2^2 = 1 + 4 = 5
     ```
   
   - For \( n = 3 \):
     
     ```math
     S(3) = 27a + 9b + 3c = 1^2 + 2^2 + 3^2 = 1 + 4 + 9 = 14
     ```
   
   Solving these equations yields:
   
   ```math
   a = \frac{1}{3}, \quad b = \frac{1}{2}, \quad c = \frac{1}{6}
   ```

3. **Form the Polynomial**

   Substitute the coefficients back into the polynomial:
   
   ```math
   S(n) = \frac{1}{3}n^3 + \frac{1}{2}n^2 + \frac{1}{6}n
   ```

4. **Factorization**

   Factor out \( n \):
   
   ```math
   S(n) = n \left(\frac{1}{3}n^2 + \frac{1}{2}n + \frac{1}{6}\right)
   ```
   
   Express each term with a common denominator of 6:
   
   ```math
   \frac{1}{3}n^2 = \frac{2}{6}n^2,\quad \frac{1}{2}n = \frac{3}{6}n,\quad \frac{1}{6} = \frac{1}{6}
   ```
   
   So,
   
   ```math
   S(n) = \frac{n(2n^2 + 3n + 1)}{6}
   ```
   
   Notice that the quadratic factors as:
   
   ```math
   2n^2 + 3n + 1 = (n+1)(2n+1)
   ```
   
   Thus, we arrive at:
   
   ```math
   S(n) = \frac{n(n+1)(2n+1)}{6}
   ```

### Why the 6?

The number 6 in the denominator arises from combining the fractional coefficients \(\frac{1}{3}\), \(\frac{1}{2}\), and \(\frac{1}{6}\) when expressed over a common denominator. It is the least common multiple (LCM) of 3 and 2, ensuring that the final formula yields an integer for any natural number \( n \).

## 2. Square of the Sum

The square of the sum of the first *n* natural numbers is calculated in two steps:

1. **Calculate the Sum:**

   The sum of the first \( n \) natural numbers is:
   
   ```math
   1 + 2 + 3 + \ldots + n = \frac{n(n+1)}{2}
   ```

2. **Square the Sum:**

   Square the result:
   
   ```math
   \left(\frac{n(n+1)}{2}\right)^2
   ```

For example, for \( n = 10 \):
- The sum is:
  
  ```math
  \frac{10 \cdot 11}{2} = 55
  ```

- Squaring this sum gives:
  
  ```math
  55^2 = 3025
  ```

## 3. Difference of Squares

The difference between the square of the sum and the sum of the squares is computed as:

```math
\text{Difference} = \left(\frac{n(n+1)}{2}\right)^2 - \frac{n(n+1)(2n+1)}{6}
```

For \( n = 10 \):
- The square of the sum is \( 3025 \).
- The sum of the squares is:
  
  ```math
  \frac{10 \cdot 11 \cdot 21}{6} = 385
  ```

- Their difference is:
  
  ```math
  3025 - 385 = 2640
  ```

## Conclusion

Understanding these derivations provides a robust methodology for tackling problems involving sums and series. The techniques of polynomial fitting, finding common denominators, and factorization are invaluable tools that extend to many areas of mathematics. This explanation not only justifies the formula for the sum of squares but also prepares you to approach similar problems in the future.

Happy learning!
---



# Verion2 inline latex


Below is an updated document that explains the mathematical formulas for calculating the difference of squares, but now using inline math (e.g., `$...$`).

---

## 1. Sum of the Squares

The sum of the squares of the first *n* natural numbers is given by:
  
The formula:  
$1^2 + 2^2 + 3^2 + \ldots + n^2 = \dfrac{n(n+1)(2n+1)}{6}$

### Derivation Outline

1. **Polynomial Form Assumption**  
   Assume the sum $S(n)$ can be expressed as a cubic polynomial:  
   $S(n) = an^3 + bn^2 + cn + d$.  

   Since $S(0) = 0$ (the sum of zero numbers is 0), it follows that $d = 0$.

2. **Determining the Coefficients**  
   Plug in small values for $n$:

   - $n = 1$:  
     $S(1) = a \cdot 1^3 + b \cdot 1^2 + c \cdot 1 = a + b + c = 1$
   - $n = 2$:  
     $S(2) = 8a + 4b + 2c = 1^2 + 2^2 = 5$
   - $n = 3$:  
     $S(3) = 27a + 9b + 3c = 1^2 + 2^2 + 3^2 = 14$

   Solving these equations yields  
   $\,a = \tfrac{1}{3}, \,\, b = \tfrac{1}{2}, \,\, c = \tfrac{1}{6}$.

3. **Form the Polynomial**  
   Substitute $a, b, c$ back into the polynomial:  
   $S(n) = \tfrac{1}{3} n^3 + \tfrac{1}{2} n^2 + \tfrac{1}{6} n$.

4. **Factorization**  
   Factor out $n$:  
   $S(n) = n \bigl(\tfrac{1}{3}n^2 + \tfrac{1}{2}n + \tfrac{1}{6}\bigr)$  

   Convert the terms inside the parentheses to a common denominator of 6:  
   $\tfrac{1}{3}n^2 = \tfrac{2}{6}n^2, \quad \tfrac{1}{2}n = \tfrac{3}{6}n, \quad \tfrac{1}{6} = \tfrac{1}{6},$  
   so  
   $S(n) = \dfrac{n \bigl(2n^2 + 3n + 1\bigr)}{6}.$  

   Note that $2n^2 + 3n + 1$ factors neatly as $(n+1)(2n+1)$, giving:  
   $S(n) = \dfrac{n(n+1)(2n+1)}{6}.$

### Why the 6?

The number 6 in the denominator results from combining fractional coefficients ($\tfrac{1}{3}, \tfrac{1}{2}, \tfrac{1}{6}$) under a common denominator. It corresponds to the least common multiple (LCM) of 2 and 3, ensuring $S(n)$ evaluates to an integer for any natural number $n$.

---

## 2. Square of the Sum

Calculating the square of the sum of the first *n* natural numbers proceeds in two steps:

1. **Compute the Sum**  
   $1 + 2 + 3 + \ldots + n = \tfrac{n(n+1)}{2}.$

2. **Square the Sum**  
   $\Bigl(\tfrac{n(n+1)}{2}\Bigr)^2.$

For example, let $n = 10$:

- The sum: $1 + 2 + \ldots + 10 = \tfrac{10 \cdot 11}{2} = 55.$  
- Squaring the sum: $(55)^2 = 3025.$

---

## 3. Difference of Squares

We define the difference of squares as:

$\text{Difference} = \Bigl(\tfrac{n(n+1)}{2}\Bigr)^2 \;-\; \dfrac{n(n+1)(2n+1)}{6}.$

For $n = 10$:

- Square of the sum: $3025.$  
- Sum of the squares: $\dfrac{10 \cdot 11 \cdot 21}{6} = 385.$  
- Their difference: $3025 - 385 = 2640.$

---

## Conclusion

1. The **sum of squares** formula $1^2 + 2^2 + \ldots + n^2 = \tfrac{n(n+1)(2n+1)}{6}$ arises from polynomial fitting and factoring.
2. The **square of the sum** involves $\bigl(\tfrac{n(n+1)}{2}\bigr)^2$.
3. **Difference of squares** is their straightforward subtraction.

Familiarity with techniques like polynomial fitting, factoring, and common denominators is invaluable for handling more advanced series and sum problems in mathematics. This understanding helps ensure correct and efficient implementation in code. 

Happy learning!
