# What are inner classes in Java

#### What are inner classes in Java? Explain with an example.

**Answer:** Inner classes are classes defined within another class. They can access the members of the outer class, including private members.

**Example:**

```java
class OuterClass {
    private String message = "Hello from OuterClass";

    class InnerClass {
        void display() {
            System.out.println(message);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        OuterClass outer = new OuterClass();
        OuterClass.InnerClass inner = outer.new InnerClass();
        inner.display(); // Outputs: Hello from OuterClass
    }
}
```
