# Daily-Leetcode-problem-solution1
PROBLEM
You are given a 0-indexed 2D matrix grid of size m x n, where (r, c) represents:
A land cell if grid[r][c] = 0, or
A water cell containing grid[r][c] fish, if grid[r][c] > 0.
A fisher can start at any water cell (r, c) and can do the following operations any number of times:
Catch all the fish at cell (r, c), or
Move to any adjacent water cell.
Return the maximum number of fish the fisher can catch if he chooses his starting cell optimally, or 0 if no water cell exists.
An adjacent cell of the cell (r, c), is one of the cells (r, c + 1), (r, c - 1), (r + 1, c) or (r - 1, c) if it exists.

APPROACH
1.Traverse the grid. Recursively visit all adjacent cells starting from starting grid (r,c).
2.Mark all visited grids as 0 because there is no point in visting them again.
3.Note the number of fish in each connected grid.
4.Once the entire grid is traversed, check the fish count with the maximum number of fish caught.
5.Update and return this value.

ANALYSIS OF TIME COMPLEXITY
Time complexity:
Traversing grid: O(m * n)
DFS: O(m * n)
Implies, Total time complexity is O(m * n)+O(m * n)=O(m*n)

Space complexity:
O(m * n)
