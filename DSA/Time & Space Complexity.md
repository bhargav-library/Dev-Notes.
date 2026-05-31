What is Time Complexity?

Time complexity measures how efficient an algorithm is as the input size increases. It's not the same as the actual time taken to run a program.

Time Complexity != Execution Time

Q) What is Linear Search?

Linear Search is a searching algorithm where we check each element of an array one by one until the required element is found or the array ends. It is called “linear” because the search happens sequentially in a straight line from the first element to the last element.

In the best case, the element is found at the very first index, so only one operation is needed. In the average case, the element is usually found somewhere around the middle of the array, so approximately `n/2` operations are required. In the worst case, the element is either present at the last index or not present at all, so we may need to check all `n` elements.

The time complexity of Linear Search is O(n) because, in the worst case, the number of operations increases linearly with the size of the array.

One important advantage of Linear Search is that it works even on unsorted arrays. Unlike algorithms such as Binary Search, Linear Search does not require the data to be sorted beforehand.

In simple terms, Linear Search means checking elements one by one until the required element is found.

