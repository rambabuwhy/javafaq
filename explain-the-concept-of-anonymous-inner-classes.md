# Explain the concept of anonymous inner classes

#### Explain the concept of anonymous inner classes in Java with an example.

**Answer:** Anonymous inner classes are inner classes without a name and are used to instantiate objects with certain "extras", such as method overrides, all in one place.

**Example:**

```java
abstract class Animal {
    abstract void makeSound();
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Animal() {
            void makeSound() {
                System.out.println("Anonymous animal sound");
            }
        };
        myAnimal.makeSound(); // Outputs: Anonymous animal sound
    }
}
```
