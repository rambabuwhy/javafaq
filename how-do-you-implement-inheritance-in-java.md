# How do you implement inheritance in Java

#### How do you implement inheritance in Java?

**Answer:** Inheritance in Java is implemented using the `extends` keyword.

```java
class Animal {
    void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.makeSound(); // Outputs: Dog barks
    }
}
```
