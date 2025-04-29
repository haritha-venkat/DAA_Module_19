# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Take an integer `n` as input which represents the number of elements in the list.  
2. Read `n` floating-point numbers from the user and store them in a list `S`.  
3. If the length of the list is more than 1, find the middle index and divide the list into two halves `l` and `r`.  
4. Recursively apply `Merge_Sort` to both halves `l` and `r`.  
5. Merge the two sorted halves by comparing elements and placing them in order back into the original list. Copy any remaining elements from `l` or `r` to the original list.

## Program:
```

Program to implement Merge Sort
Developed by: harithashree
Register Number: 212222230046
def Merge_Sort(List):
    if len(List) > 1:
        mid = len(List)//2
        l = List[:mid]
        r = List[mid:]
        Merge_Sort(l)
        Merge_Sort(r)
        i = j = k = 0
        while i < len(l) and j < len(r):
            if l[i] < r[j]:
                List[k] = l[i]
                i+=1
            else:
                List[k] = r[j]
                j+=1
            k+=1
        while len(l) > i:
            List[k] = l[i]
            i+=1
            k+=1
            
        while len(r) > j:
            List[k] = r[j]
            j+=1
            k+=1
            
n = int(input())
S = []
for i in range(n):
    S.append(float(input()))
    #S+=[float(input())]
print("Given array is")
for i in S:
    print(i,end = " ")
Merge_Sort(S)
print("\nSorted array is")
for i in S:
    print(i,end = " ")

```

## Output:

![Screenshot 2025-04-29 134357](https://github.com/user-attachments/assets/137641e3-dcd7-46d0-b363-08c152bf1a84)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
