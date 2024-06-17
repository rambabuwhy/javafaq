# Multilevel inheritance

Multilevel inheritance is a type of inheritance in Java where a class is derived from another class, which is also derived from another class, forming a chain. In other words, a class inherits from a class which is also a child class of another class. This allows for a hierarchy of classes that can extend more than one level.

#### Example of Multilevel Inheritance in Java

Here's a simple example to demonstrate multilevel inheritance:

```java
// Base class
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

// Derived class
class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

// Further derived class
class Puppy extends Dog {
    void weep() {
        System.out.println("The puppy weeps.");
    }
}

public class MultilevelInheritance {
    public static void main(String[] args) {
        Puppy puppy = new Puppy();
        
        // Methods from all levels of inheritance
        puppy.eat();   // From Animal class
        puppy.bark();  // From Dog class
        puppy.weep();  // From Puppy class
    }
}
```

#### Explanation

1. **Animal Class (Base Class):**
   * This is the top-level class with a method `eat()`.
   * `Animal` is the base class for `Dog`.
2. **Dog Class (Derived Class):**
   * This class extends `Animal`, inheriting its properties and methods.
   * It adds a new method `bark()`.
   * `Dog` is the base class for `Puppy`.
3. **Puppy Class (Further Derived Class):**
   * This class extends `Dog`, inheriting properties and methods from both `Dog` and `Animal`.
   * It adds a new method `weep()`.
4. **Multilevel Inheritance Class (Main Class):**
   * This is the class with the `main` method to test the multilevel inheritance.
   * An object of `Puppy` is created, and it can call methods from `Puppy`, `Dog`, and `Animal` classes due to multilevel inheritance.
