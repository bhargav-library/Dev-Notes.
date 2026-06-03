What is Time Complexity?

Time complexity measures how efficient an algorithm is as the input size increases. It's not the same as the actual time taken to run a program.

Time Complexity != Execution Time

Q) What is Linear Search?

Linear Search is a searching algorithm where we check each element of an array one by one until the required element is found or the array ends. It is called “linear” because the search happens sequentially in a straight line from the first element to the last element.

In the best case, the element is found at the very first index, so only one operation is needed. In the average case, the element is usually found somewhere around the middle of the array, so approximately `n/2` operations are required. In the worst case, the element is either present at the last index or not present at all, so we may need to check all `n` elements.

The time complexity of Linear Search is O(n) because, in the worst case, the number of operations increases linearly with the size of the array.

One important advantage of Linear Search is that it works even on unsorted arrays. Unlike algorithms such as Binary Search, Linear Search does not require the data to be sorted beforehand.

In simple terms, Linear Search means checking elements one by one until the required element is found.

Q) What is Binary Search?

Binary Search is a searching algorithm used to find an element in a sorted array by repeatedly dividing the search space into two halves. Instead of checking elements one by one like Linear Search, Binary Search directly checks the middle element of the array. If the middle element matches the target value, the search stops. If the target value is smaller than the middle element, the search continues only in the left half of the array. If the target value is greater, the search continues only in the right half. This process keeps repeating until the element is found or the search space becomes empty.

In the best case, the middle element itself matches the target value, so only one operation is needed. In both the average case and the worst case, the number of operations required is approximately `log₂(n)` because the search space gets reduced to half after every step.

The time complexity of Binary Search is O(\log n), which makes it much faster than Linear Search for large datasets.

One important requirement of Binary Search is that it only works on sorted arrays. If the array is not sorted, Binary Search cannot correctly determine which half to discard during the search process.

In simple terms, Binary Search repeatedly divides a sorted array into halves to quickly find the required element.

When we use Linear Search for an input size of 100, it runs 100 times, whereas Binary Search takes only 7 steps. This shows that Binary Search is more efficient. As the input size (n) increases, the way an algorithm behaves helps us understand how efficient it is. Also, the graph helps us understand that Binary Search is more efficient.

Big O Notation
It is nothing; just a symbol used to represent the worst-case complexity.

What is a Log?

A logarithm tells you how many times you need to multiply a number to reach another number.

Example:log(2)(8)

This means:
2 multiplied by itself how many times gives 8?

2 × 2 × 2 = 8 → (3 times)

So: log(2)(8)=3


