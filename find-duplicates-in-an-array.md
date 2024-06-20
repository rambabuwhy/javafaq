# Find Duplicates in an Array

#### **Find Duplicates in an Array**

```java
import java.util.HashSet;
import java.util.Set;

public class FindDuplicates {
    public static Set<Integer> findDuplicates(int[] arr) {
        Set<Integer> set = new HashSet<>();
        Set<Integer> duplicates = new HashSet<>();
        for (int num : arr) {
            if (!set.add(num)) {
                duplicates.add(num);
            }
        }
        return duplicates;
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 2, 3, 5};
        System.out.println(findDuplicates(arr)); // Output: [2, 3]
    }
}
```

* **Logic**: Use a `HashSet` to track seen elements and another `HashSet` to track duplicates.
