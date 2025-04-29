# EX 1D Linear search
## DATE:

## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.



## Algorithm:


1. Take an integer input representing the number of elements in the list.  
2. Read the input strings one by one and store them in a list `List`.  
3. Take another input `n` which is the element to be searched in the list.  
4. Call the `search` function with the list and the search element `n` as arguments.  
5. In the `search` function, iterate through each element in the list:  
6. If an element matches `n`, print that the tuple is found and exit the loop.  
7. If the loop completes without finding a match, print that the tuple is not found.
 

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: harithashree
Register Number: 212222230046
def search(List,n):
    for i in List:
        if i==n:
            print("Tuple:",n,"found")
            break
    else:
        print("Tuple:",n,"not found")
List=[input() for _ in range(int(input()))]
n=input()
search(List,n)
*/
```

## Output:

![Screenshot 2025-04-29 135426](https://github.com/user-attachments/assets/a4e93ac6-2c75-4a6b-9839-8e62bf87d13b)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
