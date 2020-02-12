## Java Diary 12.02.2020

### Theoretical part:

#### Sorting Algorithms:

* ##### Selection Sort

```
import java.util.Arrays;
class SelectionSort {
    public static void main(String[] args) {
        int[] numbers = {33, 12, 5, -4, 8, -12, 187};
        System.out.println(Arrays.toString(numbers));
        int startOfUnsorted = 0;

        while(startOfUnsorted < numbers.length) {
            // find local minimum
            int myMinimumIndex = startOfUnsorted;
            int myMinimum = numbers[myMinimumIndex];
            for (int i = startOfUnsorted; i < numbers.length; i++) {
                if (numbers[i] < myMinimum) {
                    myMinimum = numbers[i];
                    myMinimumIndex = i;
                }
            }
            // switch myMinumIndex with startOfUnsorted
            int oldFirst = numbers[startOfUnsorted];
            int newFirst = numbers[myMinimumIndex];
            numbers[myMinimumIndex] = oldFirst;
            numbers[startOfUnsorted] = newFirst;
            System.out.println(Arrays.toString(numbers));

            startOfUnsorted++;
        }
    }
}
```
### Practical part:
##### how to use printf:

            System.out.println(j + "*" + i + "=" + result);

            System.out.printf("%2d * %2d = %3d\n", j, i, result);