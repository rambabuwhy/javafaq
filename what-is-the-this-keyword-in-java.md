# What is the this keyword in Java

#### What is the `this` keyword in Java? Provide an example.

**Answer:** The `this` keyword in Java is a reference to the current object whose method or constructor is being invoked. It can be used to access fields, methods, and constructors.

**Example:**

```java
class Employee {
    private String name;
    private int id;

    public Employee(String name, int id) {
        this.name = name;
        this.id = id;
    }

    public void display() {
        System.out.println("Name: " + this.name + ", ID: " + this.id);
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee("Alice", 123);
        emp.display(); // Outputs: Name: Alice, ID: 123
    }
}
```
