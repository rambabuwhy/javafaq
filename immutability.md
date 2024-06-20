# immutability

#### Explain the concept of immutability in Java with an example.

**Answer:** An immutable object is an object whose state cannot be modified after it is created. Immutable objects are inherently thread-safe and can be shared freely between threads.

**Example:**

```java
final class ImmutableClass {
    private final String name;
    private final int age;

    public ImmutableClass(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }
}

public class Main {
    public static void main(String[] args) {
        ImmutableClass obj = new ImmutableClass("Alice", 25);
        System.out.println(obj.getName()); // Outputs: Alice
        System.out.println(obj.getAge()); // Outputs: 25
    }
}
```
