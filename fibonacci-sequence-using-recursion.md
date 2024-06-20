# Fibonacci Sequence using Recursion

* **Logic**: The Fibonacci sequence is defined recursively. The `n`-th Fibonacci number is the sum of the (`n-1`)-th and (`n-2`)-th numbers.

```java
return fibonacci(n - 1) + fibonacci(n - 2);
```

Code:

```java
public class Fibonacci {
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        return fibonacci(n - 1) + fibonacci(n - 2);
    }

    public static void main(String[] args) {
        System.out.println(fibonacci(7)); // Output: 13
    }
}

```
