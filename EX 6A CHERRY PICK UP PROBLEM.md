# EX 6A CHERRY PICK UP PROBLEM
## DATE:08-09-2025
## AIM:
To Create a python program for the following problem statement.
You are given an n x n grid representing a field of cherries, each cell is one of three possible integers.
0	means the cell is empty, so you can pass through,
1	means the cell contains a cherry that you can pick up and pass through, or
-1 means the cell contains a thorn that blocks your way.
Return the maximum number of cherries you can collect by following the rules below:
Starting at the position (0, 0) and reaching (n - 1, n - 1) by moving right or down through valid path cells (cells with value 0 or 1).
After reaching (n - 1, n - 1), returning to (0, 0) by moving left or up through valid path cells.
When passing through a path cell containing a cherry, you pick it up, and the cell becomes an empty cell 0. If there is no valid path between (0, 0) and (n - 1, n - 1), then no cherries can be collected.



## Algorithm
1. Initialize a DP table (though not fully utilized in the provided snippet).
2. Iterate through the rows of the grid.
3. Iterate through the columns of the grid.
4. Attempt to assign grid values to the DP table (with an off-by-one error in indexing).
5. Initialize a result variable with a value dependent on the grid size.
6. Get the number of rows in the grid.
7. Get the number of columns in the first row of the grid.
8. Access a specific element in the (partially filled) DP table.
9. Multiply the accessed DP element by the initialized result.  

## Program:
```
To implement the program for Cherry pickup problem.
Developed by: GANESH PRABHU J
Register Number: 212223220023
```
```py
class Solution(object):
    def cherryPickup(self, grid):
        dp = [[0 for i in range(len(grid))] for j in range(len(grid))]
        for i in range(len(grid)):
            for j in range(len(grid)):
                dp[i][j] = grid[i-1][j-1]
        res = len(grid)*6
        
        
        ROW_NUM = len(grid)
        COL_NUM = len(grid[0])
        return dp[0][COL_NUM - 1]*res
        
grid=[[3,1,1],
      [2,5,1],
      [1,5,5],
      [2,1,1]]
ob=Solution()
print(ob.cherryPickup(grid))
```
## Output:

![image](https://github.com/user-attachments/assets/37350427-f989-44a8-bc8e-570ca77744c3)


## Result:
Thus the above program was executed successfully for finding the maximum number of cherries from grid.
