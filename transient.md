# transient

#### What is the `transient` keyword in Java?

**Answer:** The `transient` keyword in Java is used to indicate that a field should not be serialized. When an object is serialized, transient fields are ignored and not included in the serialization process.

**Example:**

```java
import java.io.*;

class TransientExample implements Serializable {
    String name;
    transient int age; // This field will not be serialized

    TransientExample(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

public class Main {
    public static void main(String[] args) throws IOException, ClassNotFoundException {
        TransientExample obj = new TransientExample("Alice", 25);

        // Serialization
        FileOutputStream fos = new FileOutputStream("file.ser");
        ObjectOutputStream oos = new ObjectOutputStream(fos);
        oos.writeObject(obj);
        oos.close();

        // Deserialization
        FileInputStream fis = new FileInputStream("file.ser");
        ObjectInputStream ois = new ObjectInputStream(fis);
        TransientExample deserializedObj = (TransientExample) ois.readObject();
        ois.close();

        System.out.println("Name: " + deserializedObj.name); // Outputs: Alice
        System.out.println("Age: " + deserializedObj.age); // Outputs: 0
    }
}
```
