# Big-O Notation

Big-O tells how the work of a program grows as the input size (n) grows.

## Common complexities (from fastest to slowest)
- **O(1)**: constant. Same work no matter the input size.
  Example: `nums[0]`, `x in set`
- **O(log n)**: grows very slowly. Input is cut in half each step.
  Example: binary search (Year 2)
- **O(n)**: linear. Work grows with the input.
  Example: one loop over a list
- **O(n log n)**: a bit slower than linear.
  Example: sorting, like `sorted(nums)`
- **O(n²)**: quadratic. A loop inside a loop.
  Example: checking every pair in a list
- **O(2^n)**: exponential. Work doubles with each extra input.
  Example: naive recursive Fibonacci
- **O(n!)**: factorial. Grows the fastest.
  Example: generating all permutations of a list

## Practice

```python
def first(nums):          # O(1)
    return nums[0]

def total(nums):          # O(n)
    s = 0
    for n in nums:
        s += n
    return s

def pairs(nums):          # O(n^2)
    for a in nums:
        for b in nums:
            print(a, b)

def fib(n):               # O(2^n)
    if n <= 1:
        return n
    return fib(n - 1) + fib(n - 2)
```

## Key idea
Always ask: "If the input gets 10x bigger, how much slower does my code get?"