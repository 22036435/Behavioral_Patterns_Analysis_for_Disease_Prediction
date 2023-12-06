#Counting Sort Algorithm in Python Using OOP
    #Overall Complexity Analysis:

        The overall complexity of Counting Sort is the sum of the complexities of its individual steps.
        The initialization of the count array is O(M).
        The first for-loop, which counts each element in the input array, has a complexity of O(n).
        The second for-loop, which computes the cumulative sums, is O(M).
        The final for-loop, which places each element in its correct position, is O(n).

    #Final Complexity:

        Therefore, the overall time complexity of this Counting Sort implementation is O(n + M).
        This makes it particularly efficient when M (the range of input values) is not significantly greater than n (the number of elements to sort).

#Hoare Partition / Quick Sort Algorithm
    #Complexity Analysis:

        Pivot Selection: Constant time, O(1).
        Outer 'while True' Loop:
            This loop continues until i and j cross each other. In the worst case, this loop runs for each element in the array, making its complexity O(n) where n is the number of elements between 'p' and 'r'.
        Inner Loops for 'i' and 'j':
            These loops increment/decrement 'i' and 'j', respectively, and they each run at most 'n' times (where 'n' is the length of the sub-array). The work inside each of these loops is constant time, so each loop contributes O(n) in the worst case.
        Swap Operation:
            The swap operation inside the if statement is a constant time operation, O(1).

    #Final Complexity:
        
        Therefore, the time complexity of the hoare_partition function is O(n) in the worst case, where n is the number of elements in the sub-array being partitioned.

#Quick Sort Algorithm
    #Complexity Analysis:

        Base Case Check:
            The function checks if the array length is 0 or 1, which is a constant time operation, O(1).
        Pivot Selection:
            Choosing the last element as the pivot. This is a constant time operation, O(1).
        Partitioning:
            The list comprehensions for left and right iterate over the entire array, each having a complexity of O(n), where n is the length of the array. Since they are executed sequentially, the overall partitioning step is O(n).
        Recursive Calls:
            The function is recursively called on the left and right sub-arrays. Let's say the length of the left sub-array is k and the right sub-array is n−k−1 (excluding the pivot). The time complexity of these calls is T(k) and T(n−k−1) respectively.
        Combining Results:
            The concatenation of the sorted left part, the pivot, and the sorted right part is linear in the size of the array, so it's O(n).
    
    #Overall Complexity:

        The overall time complexity of QuickSort is more challenging to express because it depends on how balanced the partitions are in each recursive call. In the best and average cases (when partitions are balanced), QuickSort achieves O(nlogn) complexity. In the worst case (when partitions are unbalanced, such as when the smallest or largest element is consistently chosen as the pivot), it degrades to O(n^2).
