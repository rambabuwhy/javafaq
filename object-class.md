# Object class

#### What is the role of the `Object` class in Java? List some methods provided by the `Object` class.

**Answer:** The `Object` class is the root of the class hierarchy. Every class has `Object` as a superclass. Some important methods provided by the `Object` class include:

* `equals(Object obj)`: Determines whether another object is equal to this one.
* `hashCode()`: Returns a hash code value for the object.
* `toString()`: Returns a string representation of the object.
* `clone()`: Creates and returns a copy of this object.
* `finalize()`: Called by the garbage collector on an object when garbage collection determines that there are no more references to the object.
* `getClass()`: Returns the runtime class of the object.

**Example:**

```java
public class Main {
    public static void main(String[] args) {
        Object obj = new String("Hello");
        System.out.println(obj.toString()); // Outputs: Hello
        System.out.println(obj.getClass().getName()); // Outputs: java.lang.String
    }
}
```
