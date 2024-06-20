# What are abstract classes and methods

#### What are abstract classes and methods in Java? Provide an example.

**Answer:** Abstract classes cannot be instantiated and may contain abstract methods, which are methods without a body that must be implemented by subclasses.

**Example:**

```java
abstract class Animal {
    abstract void makeSound();

    void sleep() {
        System.out.println("Animal is sleeping");
    }
}

class Dog extends Animal {
    void makeSound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.makeSound(); // Outputs: Dog barks
        dog.sleep(); // Outputs: Animal is sleeping
    }
}
```
