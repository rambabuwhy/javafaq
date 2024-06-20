# instanceof

#### What are the advantages and disadvantages of using the `instanceof` operator in Java?

**Answer:** **Advantages:**

* Allows safe type casting by checking the actual type of the object at runtime.
* Helps in implementing polymorphic behavior and dynamic method dispatch.

**Disadvantages:**

* Can lead to code that is hard to maintain if overused.
* Often indicates a need for refactoring or a design pattern (like Visitor) to handle type-specific behavior.

**Example:**

```java
class Animal {
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        if (animal instanceof Dog) {
            Dog dog = (Dog) animal;
            dog.bark(); // Outputs: Dog barks
        }
    }
}
```
