# static blocks

#### What are static blocks in Java? When are they executed?

**Answer:** Static blocks are used for static initialization of a class. They are executed when the class is first loaded into memory, before any object of the class is created.

**Example:**

```java
class StaticBlockExample {
    static {
        System.out.println("Static block executed");
    }

    StaticBlockExample() {
        System.out.println("Constructor executed");
    }
}

public class Main {
    public static void main(String[] args) {
        StaticBlockExample obj = new StaticBlockExample();
        // Outputs:
        // Static block executed
        // Constructor executed
    }
}
```
