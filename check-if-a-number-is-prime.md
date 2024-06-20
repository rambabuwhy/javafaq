# Check if a Number is Prime

* **Logic**: Check divisibility from 2 up to the square root of the number. If any number divides evenly, it's not prime.

```java
for (int i = 2; i <= Math.sqrt(n); i++) {
    if (n % i == 0) return false;
}
```

#### Code:

```java
public class PrimeCheck {
    public static boolean isPrime(int n) {
        if (n <= 1) return false;
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        System.out.println(isPrime(29)); // Output: true
    }
}

```
