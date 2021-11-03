One of [[Data Structures]]

The element of the linked list is encapsulated in the Node. 
A node consists of a value but also a reference field to link the next Node. This is how elements (nodes) of the linked list are organized in a sequence. 


picture here. 

Example Node code: 

```
sturct ListNode 
{
	Data d; 
	ListNode* next; 
};
```

Features: 
** We are not able to acces a rendom element in constant time as in array. We need to traverse the list from HEAD to the TAIL and look for a Node. It takes O(n) time. 
** We can insert and delete in constant time O(n), HOWEVER if we want to insert/delete in random spot, we need to traverse the list first which may take linear (O(n)) time 

Types of lists: 
Singly-linked list 
Doubly-linked list 
Circular linked list 

Two pointer technique in Linked List .

List related problems: 
** Reverse Linked List 