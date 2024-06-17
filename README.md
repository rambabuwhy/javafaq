# Overloading vs Overriding vs Dynamic dispatch

In Java, method overloading, method overriding, and dynamic dispatch are three concepts that relate to polymorphism, a key feature of object-oriented programming. Here’s a detailed explanation of each concept with examples:

#### 1. Method Overloading

Method overloading occurs when two or more methods in the same class have the same name but different parameters (different type, number, or both). It allows methods to be called based on the argument list.

**Example:**

```java
class MathUtils {
    // Overloaded method with two int parameters
    public int add(int a, int b) {
        return a + b;
    }

    // Overloaded method with three int parameters
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    // Overloaded method with two double parameters
    public double add(double a, double b) {
        return a + b;
    }
}

public class OverloadingExample {
    public static void main(String[] args) {
        MathUtils mathUtils = new MathUtils();
        System.out.println(mathUtils.add(2, 3));       // Outputs 5
        System.out.println(mathUtils.add(2, 3, 4));    // Outputs 9
        System.out.println(mathUtils.add(2.5, 3.5));   // Outputs 6.0
    }
}
```

#### 2. Method Overriding

Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its superclass. The overridden method in the subclass should have the same name, return type, and parameters.

**Example:**

```java
class Animal {
    // Method to be overridden
    public void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    // Overriding the makeSound method
    @Override
    public void makeSound() {
        System.out.println("Dog barks");
    }
}

public class OverridingExample {
    public static void main(String[] args) {
        Animal myAnimal = new Animal();
        Animal myDog = new Dog();

        myAnimal.makeSound(); // Outputs: Animal makes a sound
        myDog.makeSound();    // Outputs: Dog barks
    }
}
```

#### 3. Dynamic Dispatch

Dynamic dispatch is a mechanism by which a call to an overridden method is resolved at runtime rather than compile-time. This allows Java to support runtime polymorphism.

**Example:**

```java
class Animal {
    public void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Cat meows");
    }
}

public class DynamicDispatchExample {
    public static void main(String[] args) {
        Animal myAnimal;
        
        myAnimal = new Dog();
        myAnimal.makeSound(); // Outputs: Dog barks
        
        myAnimal = new Cat();
        myAnimal.makeSound(); // Outputs: Cat meows
    }
}
```

#### Summary

* **Method Overloading:** Compile-time polymorphism; same method name with different parameters within the same class.
* **Method Overriding:** Runtime polymorphism; subclass provides a specific implementation for a method that is already defined in its superclass.
* **Dynamic Dispatch:** Runtime mechanism; method to be executed is determined at runtime based on the object's actual type.

These concepts help in achieving polymorphism, enhancing the flexibility and maintainability of code.
