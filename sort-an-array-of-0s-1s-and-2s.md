# Sort an Array of 0s, 1s, and 2s

#### **Sort an Array of 0s, 1s, and 2s**

```java
public class SortColors {
    public static void sortColors(int[] nums) {
        int low = 0, mid = 0, high = nums.length - 1;
        while (mid <= high) {
            switch (nums[mid]) {
                case 0:
                    swap(nums, low++, mid++);
                    break;
                case 1:
                    mid++;
                    break;
                case 2:
                    swap(nums, mid, high--);
                    break;
            }
        }
    }

    private static void swap(int[] nums, int i, int j) {
        int temp = nums[i];
        nums[i] = nums[j];
        nums[j] = temp;
    }

    public static void main(String[] args) {
        int[] nums = {2, 0, 1, 2, 1, 0};
        sortColors(nums);
        for (int num : nums) {
            System.out.print(num + " "); // Output: 0 0 1 1 2 2
        }
    }
}
```

* **Logic**: Use the Dutch National Flag algorithm to sort the array in a single pass.
