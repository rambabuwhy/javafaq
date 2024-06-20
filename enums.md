# enums

#### Explain the concept of enums in Java with an example.

**Answer:** Enums in Java are special types that represent a group of constants. They provide a way to define a collection of related constants.

**Example:**

```java
enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY
}

public class Main {
    public static void main(String[] args) {
        Day day = Day.MONDAY;
        switch (day) {
            case SUNDAY:
                System.out.println("It's Sunday!");
                break;
            case MONDAY:
                System.out.println("It's Monday!");
                break;
            // other cases
            default:
                System.out.println("Other day");
        }
    }
}
```
