# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
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
i)	#Use a linear search method to match the item in a list.
```
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
k = eval(input())
n=len(array)
array.sort()
result = linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=(low+high)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
             high=mid-1
    return-1
array = eval(input())
array.sort()
k=eval(input())
result=binarySearchIter(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binarySearchIter(arr, k, low, high):
    if high >= low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return binarySearchIter(arr, k, low, mid-1)
        else:
            return binarySearchIter(arr, k, mid+1, high)
    else:
         return-1

arr = eval(input())
arr.sort()
k = eval(input())
result=binarySearchIter(arr, k,0,len(arr)-1)
if (result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)




```
## Sample Input and Output
![linear search method sample](https://user-images.githubusercontent.com/121490575/214891975-ee0d6975-2d8f-4908-b29a-c3eaa9845c44.png)
![binary search sample](https://user-images.githubusercontent.com/121490575/214892727-6eaec3b0-29fb-45e3-ae1b-1d04e600a787.png)
![recursive method sample](https://user-images.githubusercontent.com/121490575/214892833-195a55e3-6651-41e1-a045-a4e6a80f2713.png)

##Output
![linear search method](https://user-images.githubusercontent.com/121490575/214892527-39d46a0f-7f19-4bcd-96fa-ddb427a3eb30.png)
![binary search](https://user-images.githubusercontent.com/121490575/214892956-29db21a2-b43f-4d00-a3af-5abe82acc33c.png)
![recursive method](https://user-images.githubusercontent.com/121490575/214893004-1230b6aa-89af-4a39-80bf-16b54a2f5028.png)







## Result
Thus the linear search and binary search algorithm is implemented using python programming.
