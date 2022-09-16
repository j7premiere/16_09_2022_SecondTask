### Task 6 kyu

[Task link](https://www.codewars.com/kata/514b92a657cdc65150000006)

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in. Additionally, if the number is negative, return 0 (for languages that do have them).

### My solution

```Java
public class Solution {

  public int solution(int number) {
    int sum = 0;
    for(int i = 1; i < number; i++) {
      if(0 == i % 3 || 0 == i % 5) {
        sum += i;
      }
    }
    return sum;
  }
}
```

### Favourite solution from code-wars

```Java
import java.util.stream.*;
public class Solution {
  public int solution(int number) {
    return IntStream.range(3, number).filter(n -> n % 3 == 0 || n % 5 == 0).sum();
  }
}
```

I like this solution because its the shortest solution at code-wars.

# Have a nice day!