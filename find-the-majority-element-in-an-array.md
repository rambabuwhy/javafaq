# Find the Majority Element in an Array

#### **Find the Majority Element in an Array**

```java
public class MajorityElement {
    public static int findMajorityElement(int[] nums) {
        int count = 0, candidate = 0;
        for (int num : nums) {
            if (count == 0) {
                candidate = num;
            }
            count += (num == candidate) ? 1 : -1;
        }
        return candidate;
    }

    public static void main(String[] args) {
        int[] nums = {2, 2, 1, 1, 1, 2, 2};
        System.out.println(findMajorityElement(nums)); // Output: 2
    }
}
```

* **Logic**: Use Boyer-Moore Voting Algorithm to find the majority element.
