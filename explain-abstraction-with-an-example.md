# Explain abstraction with an example

#### Explain abstraction with an example.

**Answer:** Abstraction is the concept of hiding the complex implementation details and showing only the essential features of the object.

```java
abstract class Shape {
    abstract void draw();
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing a circle");
    }
}

class Rectangle extends Shape {
    void draw() {
        System.out.println("Drawing a rectangle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape circle = new Circle();
        Shape rectangle = new Rectangle();
        circle.draw(); // Outputs: Drawing a circle
        rectangle.draw(); // Outputs: Drawing a rectangle
    }
}
```
