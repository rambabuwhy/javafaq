# Remove Duplicates from Array

* **Logic**: Use a `HashSet` to store unique elements from the array. Convert the set back to an array.

```java
Set<Integer> set = new HashSet<>();
for (int i : arr) {
    set.add(i);
}
```

Code:

```java
import java.util.Arrays;
import java.util.HashSet;
import java.util.Set;

public class RemoveDuplicates {
    public static int[] removeDuplicates(int[] arr) {
        Set<Integer> set = new HashSet<>();
        for (int i : arr) {
            set.add(i);
        }
        int[] result = new int[set.size()];
        int i = 0;
        for (int num : set) {
            result[i++] = num;
        }
        return result;
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 4, 4, 5};
        int[] result = removeDuplicates(arr);
        System.out.println(Arrays.toString(result)); // Output: [1, 2, 3, 4, 5]
    }
}

```
