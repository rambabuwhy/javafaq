# What is a static method in Java

#### What is a static method in Java? Can we override a static method?

**Answer:** A static method belongs to the class rather than instances of the class. Static methods can be called without creating an instance of the class. Static methods cannot be overridden, but they can be hidden by another static method in a subclass.

**Example:**

```java
class Parent {
    static void display() {
        System.out.println("Static method in Parent");
    }
}

class Child extends Parent {
    static void display() {
        System.out.println("Static method in Child");
    }
}

public class Main {
    public static void main(String[] args) {
        Parent.display(); // Outputs: Static method in Parent
        Child.display(); // Outputs: Static method in Child
    }
}
```
