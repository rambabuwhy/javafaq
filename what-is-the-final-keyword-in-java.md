# What is the final keyword in Java

#### What is the `final` keyword in Java? Explain its use with examples.

**Answer:** The `final` keyword in Java is used to define constants, prevent inheritance, and prevent method overriding.

**Example:**

```java
final class FinalClass {
    // This class cannot be subclassed
}

class Test {
    final int CONSTANT = 10; // This variable cannot be changed

    final void display() {
        System.out.println("This method cannot be overridden");
    }
}

class SubClass extends Test {
    // void display() { 
    // This will cause a compile-time error
    // }
}

public class Main {
    public static void main(String[] args) {
        Test test = new Test();
        System.out.println(test.CONSTANT); // Outputs: 10
    }
}
```
