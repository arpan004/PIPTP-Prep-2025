# Week1 - Day 2

# Problems

### Problem 1

Given the following pseudocode, determine what value will be printed:

```
1  Integer a, b, c
2  Set a=2, b=6, c=8
3  a=(10+9)+c
4  if((c+b)>(a-c))
5      a=b+c
6      b=b+b
7  End if
8  Print a+b+c
```

### Multiple Choice Options

- **A.** 23
- **B.** 41
- **C.** 48
- **D.** 58


### Answer

**B. 41**

### Explanation

The key insight is understanding the order of operations and conditional logic:

- In Line 3, variable `a` is updated from `2` to `27` (calculated as `(10+9)+c = 19+8 = 27`)
- In Line 4, the conditional statement evaluates the expression with the updated value of `a`
- Since `(c+b = 8+6 = 14)` is **not** greater than `(a-c = 27-8 = 19)`, the `if` body is not executed
- The program jumps directly to Line 8 and prints the sum: `a+b+c = 27+6+8 = 41`

Therefore, option **B** is the correct answer.

---

### Problem 2
```
1
2  Integer funn(Integer a, Integer b, Integer c)
3      b=7+a
4      a=(a+c)+a
5      b=(b+b)+c
6      c=1+b
7      return a+b+c
8  End function funn()
```

### Multiple Choice Options

- **A.** 59
- **B.** 68
- **C.** 70
- **D.** 39

### Approach
Follow the order of operations and variable updates step by step.
Track how each variable changes through the function execution.
Calculate the final sum of a+b+c.

### Answer

**B. 59**

### Final Solution
**A. 59**

---

### Problem 3
```
1  Integer pp, qq, rr
2  Set pp=0, qq=6, rr=7
3  pp=rr+pp
4  pp=(rr&4)^rr
5  if((qq&pp&rr)<(rr&qq))
6      if((qq^pp)<(rr+qq))
7          rr=(3+1)^pp
8      End if
9  End if
10 Print pp+qq+rr
```

### Multiple Choice Options

- **A.** 29
- **B.** 18
- **C.** 10
- **D.** 16

### Approach
Follow the step-by-step execution with bitwise operations.
Track variable updates through AND (&) and XOR (^) operations.
Evaluate nested conditional statements.
Calculate final sum.


### Final Solution
**D. 16**
