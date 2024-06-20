# What is an interface in Java

#### What is an interface in Java? How is it different from an abstract class?

**Answer:** An interface in Java is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields or constructors.

Differences between an interface and an abstract class:

* Interfaces can only declare methods; abstract classes can provide implementations.
* A class can implement multiple interfaces but can only extend one abstract class.
* Interfaces cannot have constructors, abstract classes can.

**Example:**

```java
interface Animal {
    void eat();
}

class Dog implements Animal {
    public void eat() {
        System.out.println("Dog eats");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Outputs: Dog eats
    }
}
```
