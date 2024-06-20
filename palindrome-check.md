# Palindrome Check

* **Logic**: Compare characters from the start and end of the string moving towards the center. If all characters match, it's a palindrome.

```java
while (left < right) {
    if (str.charAt(left) != str.charAt(right)) return false;
    left++;
    right--;
}
```

Code:

```java
public class PalindromeCheck {
    public static boolean isPalindrome(String str) {
        int left = 0, right = str.length() - 1;
        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) return false;
            left++;
            right--;
        }
        return true;
    }

    public static void main(String[] args) {
        System.out.println(isPalindrome("racecar")); // Output: true
    }
}

```
