# method hiding

#### Explain the concept of method hiding in Java with an example.

**Answer:** Method hiding occurs when a subclass defines a static method with the same signature as a static method in the superclass. The method in the superclass is hidden, not overridden.

**Example:**

```java
class Parent {
    static void display() {
        System.out.println("Static method in Parent");
    }
}

class Child extends Parent {
    static void display() {
        System.out.println("
```
