# Find the Length of the Longest Substring Without Repeating Characters

#### **Find the Length of the Longest Substring Without Repeating Characters**

```java
import java.util.HashSet;
import java.util.Set;

public class LongestSubstringWithoutRepeats {
    public static int lengthOfLongestSubstring(String s) {
        int n = s.length();
        Set<Character> set = new HashSet<>();
        int i = 0, j = 0, maxLength = 0;
        while (i < n && j < n) {
            if (!set.contains(s.charAt(j))) {
                set.add(s.charAt(j++));
                maxLength = Math.max(maxLength, j - i);
            } else {
                set.remove(s.charAt(i++));
            }
        }
        return maxLength;
    }

    public static void main(String[] args) {
        System.out.println(lengthOfLongestSubstring("abcabcbb")); // Output: 3 ("abc")
    }
}
```

* **Logic**: Use a sliding window and a `HashSet` to track characters in the current window.
