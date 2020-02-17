## Java Diary 17.02.2020

### Theoretical part:

#### Sorting Algorithms:

* ##### Insertion Sort
An array is always sorted in the already relatively (internally)Part S 
and the unsorted part U divided.Step by step, the first element of the 
unsortedPartly selected and put in the right place in the sorted array pushed.
The entire array is initially unsorted.

```
```

* ##### Bubble Sort
Starting from the left, there are always two on top of each other compared 
and swapped the following elements in the array if whose order is not correct.
This makes the largest element after the first iteration on the far right, 
after the second iteration, are the two largest items on the right.

```
```

* ##### Merge Sort
An array is broken down into smaller arrays, which are divided into 
sorted and merged in sorted order(with merge).

```
```
* ##### Quick Sort
As with the merge sort, the array is split with the quick sort
and the sublists are sorted. When you share it becomes aPivot element selected 
and all elements smaller than thatPivot elements are in the left half and 
those that are larger exchanged in the right half of the.
This sorting is applied to all sublists again until the complete 
list is sorted.

```
```

### Practical part:
##### Insertion Sort:
```
        int[] unsorted = {5, 4, 1, 9, 6, 7, 3, 2, 8};
        int countRight = 1;
        int countLeft = 1;
        int temp;

        while (countRight < unsorted.length) {
            for (int j = countRight; j > 0; j--) {
                if (unsorted[j] < unsorted[j - countLeft]) {
                    temp = unsorted[j];
                    unsorted[j] = unsorted[j - countLeft];
                    unsorted[j - countLeft] = temp;
                }
            }
            countRight++;
        }
        /* print the sorted array */
        for (int p : unsorted) {
            System.out.print(p + " ");
        }

    }
```