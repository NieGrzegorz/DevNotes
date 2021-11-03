One of [[Data Structures]]. 
Array is a collection of items stored in NEIGHBORIGN (contiguous) memory locations. All items are stored together. 

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
- Insert the element at the beginning of the array - 1. make a space for the item, relocate every nth item to n+1 position and remove the ones exceeding capacity, add the element to the beginning. (VERY COSTLY)
- Insert in the middle 

In place array operations: 