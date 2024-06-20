# Check if Two Strings are Rotations of Each Other

#### **Check if Two Strings are Rotations of Each Other**

```java
public class StringRotationCheck {
    public static boolean areRotations(String str1, String str2) {
        return (str1.length() == str2.length()) && (str1 + str1).contains(str2);
    }

    public static void main(String[] args) {
        System.out.println(areRotations("abcd", "dabc")); // Output: true
    }
}
```

* **Logic**: Concatenate `str1` with itself and check if `str2` is a substring of the result.
