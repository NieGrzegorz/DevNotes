# Pointers and references
Pointers and references are prominent features of C++ and one of its [[Basic features]]. 

### Pointers 
Type of variable in C++ that holds an address to a memory of a different object. Pointer is defined by syntax: 

```
	Type* varName; //Uninitialized pointer 
```

Pointers allow to access the same object in different locations without copying it. Also pointer can be reassigned so it can point to different object during its lifetime. 

### References 
Reference can be considered as an alias. A different name for the same variable. It must be initialized and cannot be reassigned. It can be used to reference the same memory from different places without making a copy. 

Reference syntax: 
```
	Type& refName = object; //refName variable points at the same memory
							// as object
```

### Pointer vs Reference 
There are eight major differences between pointers and references: 
1. Pointers may be nullptr and references cannot be assigned nullptr. But reference may be assigned a variable which is a nullptr. 
2. References cannot be stuffed into a container. 
3. While using pointer to an object we need to use "->" to access its members. In case of references we use "."; 
4. Pointers can be reassigned. References must be assigned during the initialization and cannot be reassigned. 

### Tags: 
#cppbasic