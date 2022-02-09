# Linked list
One of [[Data Structures]]

The element of the linked list is encapsulated in the Node. A node consists of a value but also a reference field to link the next Node. This is how elements (nodes) of the linked list are organized in a sequence. 


picture here. 

## Example Node code: 

```C++
sturct ListNode 
{
	Data d; 
	ListNode* next; 
};
```

## Features: 
** We are not able to acces a rendom element in constant time as in array. We need to traverse the list from HEAD to the TAIL and look for a Node. It takes O(n) time. 
** We can insert and delete in constant time O(n), HOWEVER if we want to insert/delete in random spot, we need to traverse the list first which may take linear (O(n)) time 

## Types of lists: 
- Singly-linked list 
- Doubly-linked list 
- Circular linked list 

## Two pointer technique in Linked List 
Typical problem which can be solved with two pointer technique is determining if a list has a cycle. 

### Algorithm 
- Use two pointers: **slow pointer** and **fast pointer** 
- Iterate through the list
- Move **slow pointer** one position at the time, move **fast pointer** two poistions at the time 
- If **fast pointer** ends up at the end of the list (next node is nullptr), **there is no cycle**
- If **ther is a cycle**, **fast pointer** and **slow pointer** will point at  the same node eventually. 

List related problems: 
- Reverse Linked List
- Determine if a list has a cycle  
- Intersection of two linked lists 