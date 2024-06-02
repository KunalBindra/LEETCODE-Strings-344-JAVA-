# LEETCODE-Strings-344-JAVA-
Sure, let's perform a dry run of the given `reverseString` method from the `Solution` class. This method reverses an array of characters in place.

Here's the method:

```java
class Solution {
  public void reverseString(char[] s) {
    int l = 0;
    int r = s.length - 1;

    while (l < r) {
      char temp = s[l];
      s[l++] = s[r];
      s[r--] = temp;
    }
  }
}
```

Let's step through this with an example input:

### Example Input:
`char[] s = {'h', 'e', 'l', 'l', 'o'}`

### Dry Run Steps:

1. **Initialization:**
   - `l = 0` (left index)
   - `r = 4` (right index, because `s.length - 1` is 4)

2. **First Iteration:**
   - `l < r` (0 < 4) is true.
   - `temp = s[l]` (temp = 'h')
   - `s[l] = s[r]` (s[0] = 'o', so the array is now `{'o', 'e', 'l', 'l', 'o'}`)
   - `s[r] = temp` (s[4] = 'h', so the array is now `{'o', 'e', 'l', 'l', 'h'}`)
   - `l++` (l becomes 1)
   - `r--` (r becomes 3)

3. **Second Iteration:**
   - `l < r` (1 < 3) is true.
   - `temp = s[l]` (temp = 'e')
   - `s[l] = s[r]` (s[1] = 'l', so the array is now `{'o', 'l', 'l', 'l', 'h'}`)
   - `s[r] = temp` (s[3] = 'e', so the array is now `{'o', 'l', 'l', 'e', 'h'}`)
   - `l++` (l becomes 2)
   - `r--` (r becomes 2)

4. **Third Iteration:**
   - `l < r` (2 < 2) is false, so the loop terminates.

### Final State:
The array is `{'o', 'l', 'l', 'e', 'h'}`, which is the reverse of the original array.

### Summary:
- The method successfully reverses the input character array in place.
- Each iteration swaps characters from the start and end, moving towards the center of the array.

This dry run helps to verify that the method works as intended by manually simulating its execution.
