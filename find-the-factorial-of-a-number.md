# Find the Factorial of a Number

* **Logic**: Use recursion where the factorial of `n` is `n` times the factorial of `n-1`. Base case: factorial of 0 is 1.

```java
return n * factorial(n - 1);
```

Code:

```java
public class Factorial {
    public static int factorial(int n) {
        if (n == 0) return 1;
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(factorial(5)); // Output: 120
    }
}

```
