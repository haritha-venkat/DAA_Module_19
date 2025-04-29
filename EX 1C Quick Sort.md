# EX 1C Quick Sort
## DATE:

## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm

1. Take an integer `n` as input representing the number of elements in the list.  
2. Read `n` integers from the user and store them in a list `nums`.  
3. Call the quick sort function `qs` with initial left and right indices as 0 and `n-1`.  
4. In the `qs` function, if the left index `l` is less than the right index `r`, call the `partition` function to find the pivot index `pi`.  
5. Recursively apply `qs` to the subarrays before and after the pivot index.  
6. In the `partition` function, select the first element as the pivot, and initialize pointers `i` and `j` at the left and right ends.  
7. Move pointer `i` forward until an element greater than the pivot is found, and move pointer `j` backward until an element smaller than the pivot is found.  
8. If `i` is less than or equal to `j`, swap the elements at `i` and `j`, otherwise break the loop.  
9. After the loop, swap the pivot element with the element at pointer `j`, and return `j` as the pivot index.  
10. Finally, print the sorted array `nums`.  

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: harithashree
Register Number: 212222230046
def qs(l,r,nums):
    if l<r:
        pi=partition(l,r,nums)
        qs(l,pi-1,nums)
        qs(pi+1,r,nums)
def partition(l,r,nums):
    pivot,i,j=nums[l],l,r
    print("Pivot: ",pivot)
    while True:
        while i<=j and nums[i]<=pivot:
            i+=1
        while i<=j and nums[j]>=pivot:
            j-=1
        if i<=j:
            nums[i],nums[j]=nums[j],nums[i]
        else:
            break
    nums[j],nums[l]=nums[l],nums[j]
    return j
n=int(input())
nums=[int(input()) for i in range(n)]
qs(0,n-1,nums)
print("Sorted array:",nums)
*/
```

## Output:

![Screenshot 2025-04-29 135045](https://github.com/user-attachments/assets/bc461221-4d03-4f0c-984d-e46361490a26)



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
