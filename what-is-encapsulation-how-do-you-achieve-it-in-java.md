# What is encapsulation? How do you achieve it in Java

#### What is encapsulation? How do you achieve it in Java?

**Answer:** Encapsulation is the technique of making the fields in a class private and providing access to them via public methods. This way, you can control the data.

```java
class Person {
    private String name;
    private int age;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("John");
        person.setAge(25);
        System.out.println(person.getName()); // Outputs: John
        System.out.println(person.getAge());  // Outputs: 25
    }
}
```
