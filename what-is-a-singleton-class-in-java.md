# What is a singleton class in Java

#### What is a singleton class in Java? How do you implement it?

**Answer:** A singleton class in Java is a class that allows only one instance of itself to be created and provides a global point of access to that instance.

**Example:**

```java
class Singleton {
    private static Singleton instance;

    private Singleton() {
        // Private constructor to prevent instantiation
    }

    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }

    public void display() {
        System.out.println("Singleton instance method");
    }
}

public class Main {
    public static void main(String[] args) {
        Singleton singleton = Singleton.getInstance();
        singleton.display(); // Outputs: Singleton instance method
    }
}
```
