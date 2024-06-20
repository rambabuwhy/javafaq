# Explain the concept of composition

#### Explain the concept of composition in Java with an example.

**Answer:** Composition is a design principle where a class is composed of one or more objects of other classes, allowing for code reuse and a "has-a" relationship.

**Example:**

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
