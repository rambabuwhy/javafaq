# marker interface

#### What is a marker interface in Java? Provide an example.

**Answer:** A marker interface in Java is an interface with no methods or constants. It is used to mark a class as having some property or behavior, often checked by the Java runtime or other code.

**Example:**

```java
interface Serializable {
    // No methods or fields
}

class Person implements Serializable {
    private String name;

    Person(String name) {
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person("Alice");
        if (person instanceof Serializable) {
            System.out.println("Person is serializable");
        }
    }
}
```
