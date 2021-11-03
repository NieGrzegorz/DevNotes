One of [[Data Structures]]. 
Array is a collection of items stored in NEIGHBORING (contiguous) memory locations. All items are stored together. 

** Capacity of an array - how many items can be held in the array 
** Length of an array - how many items are currently in the array

Features of array: 
** Items are stored together in contigous memory 
** Indexing starts at 0 
** The capacity of array must be decided when the Array is created. 
** Capacity of array cannot be changed later 


Array operations: 

** Insert
** Delete 
** Search 

Inserting: 
- There are some scenarios of inserting items in the array: 
- Insert at the end - just add the item to the collection as long as capacity of the array allows 
- Insert the element at the beginning of the array - 1. make a space for the item, relocate every nth item to n+1 position and remove the ones exceeding capacity, add the element to the beginning. (VERY COSTLY). This is linear time complexity  O(n), where n is the number of elements in the array. 
- Insert in the middle 
	- Similar to the insertion at the beginning, 1. find a spot to insert, shift all elements past to the right. It also is considered as costly operation since potentially almost all elements would have to be shifted. 

Deletion: 
 - As in case of insertion. The easiest and the least costly is the deletion from the end. Just erase the last element. 
 - Deletion at the beggining requires the shift of all the elements to the left. Cost is O(n) 
 - Deletion in the middle requires the shift of all elements right to the left. 

Search operations: 
Linear search - iterate throug the array looking for the element - costly, linear time 
Binary search - only if array is sorted - effictient 

In place array operations:  
- These operations are a way to minimise the time and space complexity of an algorithm. Usually encounteres in interviews 
- The gist is to modify the existing array without using extra space for 

Two pointer technique: 
- Use two pointers in the array which can move i the same direction or the opposite or with fixed width 

Circular Array: 
Connect the end of the array with the beginning. 