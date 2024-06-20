# Reverse a String

* **Logic**: The `StringBuilder` class provides a `reverse` method which reverses the sequence of characters. We convert the input string to a `StringBuilder`, reverse it, and then convert it back to a string.

```java
new StringBuilder(str).reverse().toString();
```

Code:

```java
public class ReverseString {
    public static String reverse(String str) {
        return new StringBuilder(str).reverse().toString();
    }

    public static void main(String[] args) {
        System.out.println(reverse("hello")); // Output: "olleh"
    }
}

```
