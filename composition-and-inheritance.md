# composition and inheritance

#### What is the difference between composition and inheritance in Java? Provide an example.

**Answer:**

* **Inheritance**: Establishes an "is-a" relationship between classes. A subclass inherits fields and methods from a superclass.
* **Composition**: Establishes a "has-a" relationship. A class contains references to objects of other classes as its members.

**Example: Inheritance**

```java
class Animal {
    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Outputs: Animal eats
        dog.bark(); // Outputs: Dog barks
    }
}
```

**Example: Composition**

```java
class Engine {
    void start() {
        System.out.println("Engine starts");
    }
}

class Car {
    private Engine engine;

    Car() {
        engine = new Engine();
    }

    void start() {
        engine.start();
        System.out.println("Car starts");
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car();
        car.start();
        // Outputs:
        // Engine starts
        // Car starts
    }
}
```
