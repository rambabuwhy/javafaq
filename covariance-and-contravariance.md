# covariance and contravariance

#### What is covariance and contravariance in Java? Provide an example.

**Answer:** Covariance and contravariance refer to how subtyping relationships (inheritance) are preserved in parameterized types.

* **Covariance**: Allows a method to return a type that is a subclass of the return type in the superclass. Java supports covariant return types.
* **Contravariance**: Allows a method to accept parameters of a type that is a superclass of the parameter type in the superclass. Java does not support contravariant method parameters but allows it with generics through wildcards.

**Example: Covariance**

```java
class Parent {
    Parent getObject() {
        return this;
    }
}

class Child extends Parent {
    @Override
    Child getObject() {
        return this;
    }
}

public class Main {
    public static void main(String[] args) {
        Parent obj = new Child().getObject();
        System.out.println(obj.getClass().getName()); // Outputs: Child
    }
}
```

**Example: Contravariance with Generics**

```java
import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<? super Integer> list = new ArrayList<Number>();
        list.add(10);
        System.out.println(list.get(0)); // Outputs: 10
    }
}
```
