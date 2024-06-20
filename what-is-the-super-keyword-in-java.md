# What is the super keyword in Java

#### What is the `super` keyword in Java? How is it used?

**Answer:** The `super` keyword in Java is used to refer to the immediate parent class object. It can be used to call parent class methods, access parent class fields, and invoke parent class constructors.

**Example:**

```java
class Parent {
    String name = "Parent";

    void display() {
        System.out.println("Display method in Parent");
    }
}

class Child extends Parent {
    String name = "Child";

    void display() {
        super.display();
        System.out.println("Display method in Child");
    }

    void showNames() {
        System.out.println("Name in Parent: " + super.name);
        System.out.println("Name in Child: " + this.name);
    }
}

public class Main {
    public static void main(String[] args) {
        Child child = new Child();
        child.display();
        child.showNames();
        // Outputs:
        // Display method in Parent
        // Display method in Child
        // Name in Parent: Parent
        // Name in Child: Child
    }
}
```
