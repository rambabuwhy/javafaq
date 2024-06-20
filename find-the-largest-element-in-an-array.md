# Find the Largest Element in an Array

```java
public class LargestElement {
    public static int findLargest(int[] arr) {
        int max = arr[0];
        for (int i : arr) {
            if (i > max) max = i;
        }
        return max;
    }

    public static void main(String[] args) {
        int[] arr = {2, 8, 1, 5, 13, 7};
        System.out.println(findLargest(arr)); // Output: 13
    }
}

```
