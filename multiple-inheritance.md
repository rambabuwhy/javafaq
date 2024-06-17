# multiple inheritance

In Java, multiple inheritance refers to a feature where a class can inherit properties and behaviors from more than one parent class. Java does not support multiple inheritance with classes directly due to the "diamond problem," where ambiguity can arise if multiple parent classes have methods with the same signature. However, Java provides mechanisms to achieve multiple inheritance through interfaces and default methods.

#### Multiple Inheritance with Interfaces

In Java, a class can implement multiple interfaces. This allows a class to inherit abstract methods from multiple sources, providing a way to achieve multiple inheritance.

**Example:**

```java
interface A {
    void methodA();
}

interface B {
    void methodB();
}

class C implements A, B {
    @Override
    public void methodA() {
        System.out.println("Method A");
    }

    @Override
    public void methodB() {
        System.out.println("Method B");
    }

    public static void main(String[] args) {
        C obj = new C();
        obj.methodA();
        obj.methodB();
    }
}
```

In this example, class `C` implements both `A` and `B` interfaces, inheriting methods from both.

#### Multiple Inheritance with Default Methods in Interfaces

Java 8 introduced default methods in interfaces, which provide a way for interfaces to include method implementations. This feature helps in avoiding the diamond problem while still providing some form of multiple inheritance.

**Example:**

```java
interface A {
    default void display() {
        System.out.println("Display from A");
    }
}

interface B {
    default void display() {
        System.out.println("Display from B");
    }
}

class C implements A, B {
    @Override
    public void display() {
        A.super.display(); // or B.super.display()
    }

    public static void main(String[] args) {
        C obj = new C();
        obj.display();
    }
}
```

In this example, both interfaces `A` and `B` have a default method `display()`. Class `C` implements both interfaces and must provide its own implementation of `display()` to resolve the conflict. It can call the `display()` method of either interface using `A.super.display()` or `B.super.display()`.

#### Summary

* **Java does not support multiple inheritance with classes** to avoid the diamond problem.
* **Java supports multiple inheritance through interfaces,** where a class can implement multiple interfaces.
* **Java 8 introduced default methods** in interfaces, allowing interfaces to have method implementations and providing a form of multiple inheritance while avoiding ambiguity.

This approach helps Java maintain simplicity and avoid potential issues related to multiple inheritance while still offering flexibility through interfaces.
