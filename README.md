# What is polymorphism in Java

#### What is polymorphism in Java? Provide an example.

**Answer:** Polymorphism in Java is the ability of an object to take on many forms. It allows one interface to be used for a general class of actions.

```java
class Animal {
    void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Dog barks");
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
        Animal myDog = new Dog();
        Animal myCat = new Cat();
        myDog.makeSound(); // Outputs: Dog barks
        myCat.makeSound(); // Outputs: Cat meows
    }
}
```
