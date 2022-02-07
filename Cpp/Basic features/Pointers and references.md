# Pointers and references
Pointers and references are prominent features of C++ and one of its [[Basic features]]. 

### Pointers 
Type of variable in C++ that holds an address to a memory of a different object. Pointer is defined by syntax: 

```C++
	Type* varName; //Uninitialized pointer 
```

Pointers allow to access the same object in different locations without copying it. Also pointer can be reassigned so it can point to different object during its lifetime. 

### References 
Reference can be considered as an alias. A different name for the same variable. It must be initialized and cannot be reassigned. It can be used to reference the same memory from different places without making a copy. 

Reference syntax: 
```C++
	Type& refName = object; //refName variable points at the same memory
							// as object
```

### Pointer vs Reference 
There are eight major differences between pointers and references: 
1. Pointers may be **nullptr** and references cannot be assigned **nullptr.** But reference can hold address of pointer which is a nullptr. 
2. References cannot be stuffed into a container. 
3. Pointer has to be dereferenced via '\*'  operator to access the memory location it points to, and pointer to struct/class uses '->' operator to access members. Reference can be used directly and always uses '.' to access members of struct/class
4. Pointers can be reassigned. References must be assigned during the initialization and cannot be reassigned. 
5. Pointer has its own memory address and size on stack. Reference shares memory address with original variable but also has some space on stack. 
6. Pointers offer multiple levels of indirection (pointer to pointer). Reference offers only one level of indirection. 
7. Pointers have arythmetics. 
8. Const reference may be bound to temps as in: 
```C++
const int& ref = int(12); // this is ok! 
```

### Tags: 
#cppbasic