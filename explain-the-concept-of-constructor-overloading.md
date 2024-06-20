# Explain the concept of constructor overloading

#### Explain the concept of constructor overloading with an example.

**Answer:** Constructor overloading in Java is the ability to have more than one constructor in a class, each with different parameters.

```java
class Employee {
    private String name;
    private int id;

    // Default constructor
    public Employee() {
        this.name = "Unknown";
        this.id = 0;
    }

    // Parameterized constructor
    public Employee(String name, int id) {
        this.name = name;
        this.id = id;
    }

    public void display() {
        System.out.println("Name: " + name + ", ID: " + id);
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp1 = new Employee();
        Employee emp2 = new Employee("Alice", 123);
        emp1.display(); // Outputs: Name: Unknown, ID: 0
        emp2.display(); // Outputs: Name: Alice, ID: 123
    }
}
```
