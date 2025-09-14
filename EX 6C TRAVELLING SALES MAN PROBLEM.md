# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE:08-09-2025
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm

1. **Input** graph and start vertex `s`.
2. **List all vertices** except `s` in `vertex[]`.
3. **Generate all permutations** of `vertex[]`.
4. **Initialize** `min_path` to infinity.
5. **For each permutation**, set `current_pathweight = 0`.
6. **Traverse path** from `s` through all cities in the permutation.
7. **Add return cost** back to starting vertex.
8. **Update min\_path** if current path is shorter.
9. **Return min\_path** as the shortest route covering all cities and returning to `s`.

## Program:
```
To implement the program for TSP.
Developed by: GANESH PRABHU J
Register Number: 212223220023
```
```PY
from sys import maxsize
from itertools import permutations
V = 4
def travellingSalesmanProblem(graph, s):
    vertex =[]
    for i in range(V):
        if i !=s:
            vertex.append(i)
    min_path = maxsize
    next_permutation = permutations(vertex)
    for i in next_permutation:
        current_pathweight = 0
        k = s
        for j in i:
            current_pathweight += graph[k][j]
            k = j
        current_pathweight += graph[k][s]
        min_path = min(min_path, current_pathweight)
        
    return min_path

if __name__ == "__main__":
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s))
```
## Output:

![image](https://github.com/user-attachments/assets/dc21adeb-9ea9-4d94-9600-aebd1cad1973)


## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
