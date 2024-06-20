# finalize() method

#### What is the `finalize()` method in Java? When is it called?

**Answer:** The `finalize()` method is called by the garbage collector before an object is removed from memory. It provides a chance to clean up resources, like closing files or releasing memory.

**Example:**

```java
class Resource {
    @Override
    protected void finalize() throws Throwable {
        System.out.println("Resource is being finalized");
        super.finalize();
    }
}

public class Main {
    public static void main(String[] args) {
        Resource res = new Resource();
        res = null;
        System.gc(); // Requesting garbage collection
        // Outputs: Resource is being finalized
    }
}
```
