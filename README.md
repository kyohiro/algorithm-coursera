Algorithm Course
===========

Week1 - Percolation
-----------------------------------  
Import algs4.jar and stdlib.jar into classpath.

This implementation extends the original WeightedQuickUnionUF class. 
When unioning two grids, will judge additionally whether the groups are connected to bottom or top.
Thus if two groups are connecting to the bottom or top in the same time, the the whole system percolates.

This implementation resolves the backwash issue when using a virtual top and virtual bottom to check percolation.
And has a quite similar memory consumption, but less time consumption, compared to add another WeightedQuickUnionUF object, connecting to virtual top only.

Week2 - Queues
-----------------------------------  
Remember to clean up unreferenced objects when deleting nodes to avoid loitering.

Week3 - Collinear
-----------------------------------  
The major concern is how to determine if the points combination is already kept.

Here we calculate hash code of the list of sorted points in a line, and keep them in a hashmap.

The Fast algorithm will always return the full line but not a subsegment, so as long as the array is sorted, there is no need to worry if same combination would have different hash code.

Week4 - 8 Puzzles
-----------------------------------  
To avoid calculating a non-solvable board, wasting too many time, we adopt the approach that:
Solve the input board and its twin board simultaneously. 

If the twin board (created by flipping two neighbour grids in a row) gets solved successfully, then the input board is not solvable.

Week5 - Kd Tree
----------------------------------- 
The most inportant pruning approach for nearest method - check the points locates on which side, and run that side first.
This helps avoid majority of useless tests.

Week6 - Wordnet
-----------------------------------
To search for the shortest ancestor, do BFS starting from the two sources. Time complexity would still be E+V.



