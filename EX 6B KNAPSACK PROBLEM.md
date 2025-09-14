# EX 6B KNAPSACK PROBLEM
## DATE:8-09-2025
## AIM:
To demonstrate a python program using dynamic programming for 0/1 knapsack problem.


## Algorithm


1. **Start** with `W`, `val[]`, `wt[]`, and `n`.
2. **If** `n == 0` or `W == 0`, **return** 0.
3. **If** `wt[n-1] > W`, **recur** with `n-1` and `W`.
4. **Else**, consider item `n-1`.
5. **Include** it: add `val[n-1]` and recur with `W - wt[n-1]` and `n-1`.
6. **Exclude** it: recur with `W` and `n-1`.
7. **Take max** of include and exclude cases.
8. **Return** that maximum value.
9. **Print** final result as max value in knapsack of capacity `W`.


## Program:
```
To implement the program for 0/1 knapsack problem.
Developed by: GANESH PRABHU J
Register Number: 212223220023
```
```PY
def knapSack(W, wt, val, n):
    if n==0 or W==0:
        return 0
    if(wt[n-1] > W):
        return knapSack(W, wt, val, n-1)
    else:
        return max(val[n-1]+knapSack(W-wt[n-1], wt, val, n-1), knapSack(W, wt, val, n-1))

x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))
n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
```
## Output:

![image](https://github.com/user-attachments/assets/7aad55a7-a73f-4abe-8a16-339a1a4120bf)


## Result:
Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity .
