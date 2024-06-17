# compare objects

In Java, the `equals()`, `toString()`, and `hashCode()` methods are fundamental to how objects are compared, represented as strings, and used in collections. Here's an overview of each method:

#### `equals()`

The `equals()` method is used to determine if two objects are equal. By default, the `equals()` method in the `Object` class compares object references to check for equality (i.e., it checks if the two references point to the same object).

To compare the contents of two objects for equality, you need to override the `equals()` method in your class. The general contract for the `equals()` method includes:

1. **Reflexive**: For any non-null reference value `x`, `x.equals(x)` should return `true`.
2. **Symmetric**: For any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
3. **Transitive**: For any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
4. **Consistent**: For any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
5. **Non-nullity**: For any non-null reference value `x`, `x.equals(null)` should return `false`.

Example:

```java
public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;
        Person person = (Person) obj;
        return age == person.age && name.equals(person.name);
    }
}
```

#### `toString()`

The `toString()` method returns a string representation of the object. The default implementation in the `Object` class returns a string that consists of the class name followed by the `@` character and the object's hashcode in hexadecimal.

To provide a more meaningful string representation of your object, you can override the `toString()` method.

Example:

```java
@Override
public String toString() {
    return "Person{name='" + name + "', age=" + age + '}';
}
```

#### `hashCode()`

The `hashCode()` method returns an integer hash code value for the object. The general contract for `hashCode()` is:

1. **Consistency**: During a single execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons is modified.
2. **Equal objects must have equal hash codes**: If two objects are equal according to the `equals(Object)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
3. **Unequal objects should produce different hash codes**: It is not required that if two objects are unequal according to the `equals(java.lang.Object)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

Example:

```java
@Override
public int hashCode() {
    return Objects.hash(name, age);
}
```

#### Putting It All Together

Here’s an example of a class that correctly overrides `equals()`, `hashCode()`, and `toString()`:

```java
import java.util.Objects;

public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;
        Person person = (Person) obj;
        return age == person.age && name.equals(person.name);
    }

    @Override
    public int hashCode() {
        return Objects.hash(name, age);
    }

    @Override
    public String toString() {
        return "Person{name='" + name + "', age=" + age + '}';
    }

    // getters and setters if needed
}
```

This class now provides meaningful implementations of `equals()`, `hashCode()`, and `toString()`, which are crucial for its correct behavior in collections and debugging.
