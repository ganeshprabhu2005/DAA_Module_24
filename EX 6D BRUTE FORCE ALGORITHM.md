# EX 6D BRUTE FORCE ALGORITHM
## DATE:08-09-2025
## AIM:
To write a python program using brute force method of searching for the given substring in the main string.



## Algorithm

1. **Input** the main string `str1` and the substring `str2`.
2. **Compile** `str2` into a regex pattern using `re.compile()`.
3. **Search** for the first occurrence of the pattern in `str1`.
4. **While match exists**, do the following:
5. **Print** the start index of the current match.
6. **Search again** for the pattern starting after the last match.
7. **Repeat** the search until no match is found.
8. **End loop** when `pattern.search()` returns `None`.
9. **Terminate** after printing all match indices.

## Program:
```
To implement the program using brute force method of searching for the given substring in the main string.
Developed by: GANESH PRABHU J
Register Number: 212223220023
```
```PY
import re
def match(string,sub):
    pattern=re.compile(str2)
    r=pattern.search(str1)
    while r:
        print("Found at index {}".format(r.start()))
        r=pattern.search(str1,r.start()+1)

str1=input()
str2=input()

```
## Output:

![image](https://github.com/user-attachments/assets/5c7bc70c-61d2-4398-aff9-34efb39afa23)


## Result:
Thus the above program was executed successfully for searching the substring at respective index.
