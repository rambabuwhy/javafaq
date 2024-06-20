# shallow copy and deep copy

#### What is the difference between shallow copy and deep copy in Java?

**Answer:**

* **Shallow Copy**: Copies the references of the objects, so the copied object points to the same memory location.
* **Deep Copy**: Creates a new object and copies all the fields, recursively copying any objects referenced by the fields.

**Example:**

```java
class Address {
    String city;
    Address(String city) {
        this.city = city;
    }
}

class Person implements Cloneable {
    String name;
    Address address;

    Person(String name, Address address) {
        this.name = name;
        this.address = address;
    }

    protected Object clone() throws CloneNotSupportedException {
        // Shallow copy
        return super.clone();
    }

    protected Person deepClone() {
        // Deep copy
        return new Person(name, new Address(address.city));
    }
}

public class Main {
    public static void main(String[] args) throws CloneNotSupportedException {
        Address address = new Address("New York");
        Person p1 = new Person("John", address);
        Person p2 = (Person) p1.clone();
        Person p3 = p1.deepClone();

        p1.address.city = "Los Angeles";
        System.out.println(p2.address.city); // Outputs: Los Angeles (Shallow copy)
        System.out.println(p3.address.city); // Outputs: New York (Deep copy)
    }
}
```
