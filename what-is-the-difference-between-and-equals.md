# What is the difference between == and equals()

#### What is the difference between `==` and `equals()` method in Java?

**Answer:**

* `==` checks for reference equality (whether two references point to the same object in memory).
* `equals()` method checks for value equality (whether two objects are logically "equal").

**Example:**

```java
public class Main {
    public static void main(String[] args) {
        String s1 = new String("Hello");
        String s2 = new String("Hello");

        System.out.println(s1 == s2); // Outputs: false
        System.out.println(s1.equals(s2)); // Outputs: true
    }
}
```
