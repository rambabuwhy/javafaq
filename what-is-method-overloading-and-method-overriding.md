# What is method overloading and method overriding

#### What is method overloading and method overriding?

**Answer:**

* **Method Overloading**: Multiple methods with the same name but different parameters.
* **Method Overriding**: Subclass provides a specific implementation of a method already defined in its superclass.

**Method Overloading Example:**

```java
class MathUtils {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        MathUtils math = new MathUtils();
        System.out.println(math.add(2, 3)); // Outputs: 5
        System.out.println(math.add(2.5, 3.5)); // Outputs: 6.0
    }
}
```

**Method Overriding Example:**

```java
class Animal {
    void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Cat extends Animal {
    @Override
    void makeSound() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Cat();
        myAnimal.makeSound(); // Outputs: Cat meows
    }
}
```
