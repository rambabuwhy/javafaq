# Find Missing Number in an Array

#### **Find Missing Number in an Array**

```java
public class MissingNumber {
    public static int findMissing(int[] arr, int n) {
        int total = n * (n + 1) / 2;
        int sum = 0;
        for (int num : arr) {
            sum += num;
        }
        return total - sum;
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 4, 5, 6};
        System.out.println(findMissing(arr, 6)); // Output: 3
    }
}
```

* **Logic**: Calculate the expected sum of numbers from 1 to `n` and subtract the actual sum of the array elements to find the missing number.
