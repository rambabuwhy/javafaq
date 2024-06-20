# access modifiers

#### What are the access modifiers in Java?

**Answer:** Java provides four access modifiers to set access levels for classes, variables, methods, and constructors:

* **public**: Accessible from any other class.
* **protected**: Accessible within the same package and subclasses.
* **default** (no modifier): Accessible only within the same package.
* **private**: Accessible only within the defined class.

**Example:**

```java
class AccessModifiers {
    public int publicVar = 1;
    protected int protectedVar = 2;
    int defaultVar = 3;
    private int privateVar = 4;

    public void publicMethod() {}
    protected void protectedMethod() {}
    void defaultMethod() {}
    private void privateMethod() {}
}

public class Main {
    public static void main(String[] args) {
        AccessModifiers obj = new AccessModifiers();
        System.out.println(obj.publicVar); // Accessible
        System.out.println(obj.protectedVar); // Accessible within the same package
        System.out.println(obj.defaultVar); // Accessible within the same package
        // System.out.println(obj.privateVar); // Not accessible
    }
}
```
