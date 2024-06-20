# What is the difference between an interface and an abstract class

#### What is the difference between an interface and an abstract class in Java?

**Answer:**

* **Interface**: Can only declare methods, all fields are public static final, supports multiple inheritance.
* **Abstract Class**: Can have method implementations, non-final fields, constructors, and only supports single inheritance.

**Example for interface:**

```java
interface Animal {
    void makeSound();
}

class Dog implements Animal {
    public void makeSound() {
        System.out.println("Dog barks");
    }
}
```

**Example for abstract class:**

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
```
