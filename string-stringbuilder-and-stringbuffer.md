# String, StringBuilder, and StringBuffer

#### What is the difference between `String`, `StringBuilder`, and `StringBuffer` in Java?

**Answer:**

* **String**: Immutable sequence of characters.
* **StringBuilder**: Mutable sequence of characters, not thread-safe.
* **StringBuffer**: Mutable sequence of characters, thread-safe (synchronized).

**Example:**

```java
public class Main {
    public static void main(String[] args) {
        String str = "Hello";
        str += " World";
        System.out.println(str); // Outputs: Hello World

        StringBuilder sb = new StringBuilder("Hello");
        sb.append(" World");
        System.out.println(sb); // Outputs: Hello World

        StringBuffer sbf = new StringBuffer("Hello");
        sbf.append(" World");
        System.out.println(sbf); // Outputs: Hello World
    }
}
```
