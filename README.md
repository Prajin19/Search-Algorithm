# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Linear Search:
### (i).  
Start from the leftmost element of array[] and compare k with each element of array[] one by one.
### (ii).
If k matches with an element in array[] , return the index.
### (iii).  
If k doesn’t match with any of elements in array[], return -1 or element not found.
### Binary Search:
### (i).  
Set two pointers low and high at the lowest and the highest positions respectively.
### (ii). 
Find the middle element mid of the array ie. arr[(low + high)/2]
### (iii).
If x == mid, then return mid.Else, compare the element to be searched with m.
### (iv).
If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
### (v).
Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
### (vi).
Repeat steps 2 to 5 until low meets high
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
### i)	Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: Prajin S
RegisterNumber: 23012918
'''
def linearSearch(array,n,k):
    for i in range(n):
        if array[i]==k:
            return i
    return -1
array=eval(input())
array.sort()
k=eval(input())
n=len(array)
print(array)
result= linearSearch(array,n,k)
if result==-1:
    print('Element not found')
else:
    print('Element found at index: ',result)
```
### ii)	 Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Prajin S
RegisterNumber: 23012918
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array=eval(input())
array.sort()
k = eval(input())
print(array)
result= binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print('Element not found')
else:
    print('Element found at index: ',result)
```
### iii)Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Prajin S
RegisterNumber: 23012918
'''
def BinarySearch(arr, k, low, high):
   if high>=low:
       mid=low+(high-low)//2
       if mid==k:
           return arr.index(mid)
       elif mid<k:
            low=mid+1
            return BinarySearch(arr,k,low,high)
       elif mid>k:
            high=mid-1
            return BinarySearch(arr,k,low,high)
   return -1
arr=eval(input())
arr.sort()
low=arr[0]
high=arr[-1]
k=eval(input())
result=BinarySearch(arr,k,low,high)
if result==-1:
    print(arr)
    print('Element not found')
else:
    print(arr)
    print('Element found at index: ',result)
            
```
## Sample Input and Output

### (i)
![Screenshot 2023-12-30 130833](https://github.com/Prajin19/Search-Algorithm/assets/144979377/61eab9a4-cdad-4c9a-b8f8-92ad3c430da3)
### (ii)
![Screenshot 2023-12-30 130907](https://github.com/Prajin19/Search-Algorithm/assets/144979377/6d0a00b3-7e39-4c32-9b8a-1681cce53425)
### (iii)
![Screenshot 2023-12-30 130939](https://github.com/Prajin19/Search-Algorithm/assets/144979377/0965fb1d-d111-4f9d-aaa6-413e54e97be8)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
