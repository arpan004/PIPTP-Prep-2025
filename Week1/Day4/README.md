# Week1 - Day 4

# Problems
## Problem 1

```java
public static int f(int n) {
    if (n == 0) return 0;
    return n + f(n - 1);
}

System.out.println(f(5));
```

**What will be the output?**
- A) 15
- B) 10  
- C) 5
- D) 25

### Step-by-Step Analysis:

1. **Base Case**: When `n == 0`, the function returns 0
2. **Recursive Case**: For any positive n, the function returns `n + f(n-1)`
3. This creates a chain of recursive calls until it reaches the base case

### Trace Through f(5):

Let's trace the execution step by step:

```
f(5) calls:
├── return 5 + f(4)
    ├── f(4) calls:
        ├── return 4 + f(3)
            ├── f(3) calls:
                ├── return 3 + f(2)
                    ├── f(2) calls:
                        ├── return 2 + f(1)
                            ├── f(1) calls:
                                ├── return 1 + f(0)
                                    ├── f(0) returns 0 ✓ (base case)
```

### Working Backwards (Stack Unwinding):

```
f(0) = 0
f(1) = 1 + f(0) = 1 + 0 = 1
f(2) = 2 + f(1) = 2 + 1 = 3
f(3) = 3 + f(2) = 3 + 3 = 6
f(4) = 4 + f(3) = 4 + 6 = 10
f(5) = 5 + f(4) = 5 + 10 = 15
```

### Final Solution

**Answer: A) 15**

## Problem 2

```java
public static int foo(int n) {
    if (n == 1) return 1;
    if (n % 2 == 0) return 2 * foo(n / 2);
    return 2 * foo((n - 1) / 2) + 1;
}

System.out.println(foo(5));
```

**What will be the output?**

### Approach to Solve

This recursive function calculates values based on a **divide-and-conquer** approach with different handling for even and odd numbers.

### Function Logic:
1. **Base Case**: If `n == 1`, return 1
2. **Even Case**: If n is even, return `2 * foo(n/2)`
3. **Odd Case**: If n is odd, return `2 * foo((n-1)/2) + 1`

### Step-by-Step Trace for foo(5):

```
foo(5) calls:
├── n = 5 (odd number)
├── return 2 * foo((5-1)/2) + 1
├── return 2 * foo(4/2) + 1
├── return 2 * foo(2) + 1
    ├── foo(2) calls:
        ├── n = 2 (even number)  
        ├── return 2 * foo(2/2)
        ├── return 2 * foo(1)
            ├── foo(1) calls:
                ├── n = 1 (base case)
                ├── return 1 ✓
```

### Working Backwards (Stack Unwinding):

```
foo(1) = 1                                    (base case)
foo(2) = 2 * foo(1) = 2 * 1 = 2             (even case)
foo(5) = 2 * foo(2) + 1 = 2 * 2 + 1 = 5     (odd case)
```
## Final Solution

**Answer: 5**

