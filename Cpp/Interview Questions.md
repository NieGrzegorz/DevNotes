[[Contents - START HERE]]

### Cpp General questions
1. References vs pointers
2. What is virtual function 
3. What is early dispatch, early binding and late binding
	Dispatching - finding right method to call.  
	Late binding, dynamic binding, dynamic dispatch - runtime plymorphism 
		It happens when virtual keyword is used in method declaration, cpp creates virtual table which is look-up table for calling such methods 
	Early binding - compile time polymorphism 
4. Can we delete this? 
	Yes, we can delete this
Can we call destructor explicitly?  - Yes 
5. What are VTABLE and VPTR 

	VTABLE is mechanism to support late binding.
6. Access specifiers in C++ 
	private, public and protected 

7. Major C++ features 
	Generic programming - templates 
	OOP paradigm 	

8. Malloc and free vs new and delete 
New/delete: 
	Memory allocated from Free Store 
	Returns a fully typed pointer 
	new never returns null - it throws exception on failure 
	Has version to handle arrays 
	Can add a new memory allocator to deal with low memory (set_new_handler) 
	Can be overriden legally 
	Constructor/destructor is called 

malloc/free
	Memory allocated from heap 
	Returns a void* 
	Must specify the size required in bytes 
	Realocating larger chunk of memory is simple (no copy constructor) 
	They WONT call new/delete 

Free Strore vs Heap: 
 - Free Store and heap are not interchangable 
 - They are separate concepts but they exist in the same memory region 
 - HEap is managed with malloc/free
 - Free store is managed with new/delete

What happens during a function call: 
	- cpu stores the memory address which called
	- copies arguments to stack
	- and transfers control to a fuction
	- executes the function code
	- Returns control to the caller

9. Inline functions 
	- A request, it is not 100% sure that function will be inlined 
	- Good to use with small simple functions which are used often- to avoid overhead 
	- In small functions overhead takes more time than executing the function
	- When function is succesfully inlined, body of the function is inserted at compile time

pros:
	- Function call overhead will not occur
	- Stack pushing/poping overhead will be eliminated
dis: 
	- additional use of registers
	- may increase compilation time
	- code size increases, binary is bigger- bad for embedded 

Macro vs inline: 
	- Macros should not be used 
	- Macros cannot access private members
	- With macros compiler doesn't do type checking

10. Friend class and function in C++ 
	- Can access private and protected class members if defined as a frinen 
	- Use wisely since it violates the encapsulation 
	- Friendship is not mutual and is not inherited

Operator overloadng
	- Giving special meaning to user defined type 

11. Function overloading vs operator overloading 
	- Overloading having functions with the same name but different parameters 
	- Different types of arguments or different number of arguments 

Types of constructors: 
	- Default constructor (Zero argument constructor) 
		- if not provided, compiler will provide it
	- Copy constructor 
	- Conversion constructor 
	- Move constructor 
	- Explicit constructor

12. Copy constructor 
13. What is inheritance 
14. What is static
	- one object is alocated for a class 
	- State is saved between function calls 
	- object visibility is limited to a file 
	- should be called by means of class not an object 

15. What is namespace? 
	- It is a scope use to logically organize objects 
	- Nameless namespaces - visible only within a file 

	- generic type in C++ 
	- We may have genric classes and methods 

	- unnamed function 
	- Beneth - a class is generated with overloaded operator () 


	- So called smart pointers 
	- They release memory 
	- They allocate memory on free store 

	- Rvalue cast 

15. What happens when C++ program is executed ? 
	- https://stackoverflow.com/questions/1204078/what-happens-when-you-run-a-program

16. Difference between static and dynamic library ? 
	- Static library - linked in compiletime 
	- dynamic library - linked in runtime 

17. Compilation vs linking 
	- Compilation process 

What is polimorphism. (runtime polymorphism) 

Functor: 
	- Function object 
	- Class which has overloaded operator () 
	- Customizable, may contain states 
	- You may pass functors to algorithms (std::transform) 
----------------------------------------------------------
15. What is template 
16. What is lambda 
17. What is std::unique_ptr and std::shared_ptr and how they are used? 
18. What does std::move do 
19. What is RAII
20. What is Undefined Behavior 
21. What is Linkage
22. How to enable warning on gcc/clang/msvc
23. How are template functions represented in the virtual table 
24. 0/3/5 constructor rule 
25. What is rvalue -> what is move semantics, borrowing system
26. What is constexpr
27. What is const reference, why use it, what is a const method 
28. Stack vs heap; what is faster? 
29. Cache in C++ 
30. Co jest szybsze inline czy macro
31. What is polymorphic class - a class that defines or inherits at least one virtual function. 

https://encelo.github.io/notes.html

What happens if destructor is not virtual in base class? 
Why do we need encapsulation? -> we can trace on call stack that setter was called

## Candera questions 
Candera questions 

What is the meaning of pure virtual 
Is it good idea to call virtual methods in a destructor 
Is it good idea to throw exceptions in a destructor
	- No, destructors should never throw 

Consts in cpp  
	- return values 
	- parameters 
	- methods 

Parameter differences 
	- pointer 
	- reference 
	- call-by-value 

----------------Constructors--------------------
What is default constructor 
What is copy constructor 
What is converting/conversion constructor 
What is move-constructor


Cast types in C++
What is a functor 
What is ownership 
	Is there a garbage collector in C++ 
	Are there alternatives? 

What is move semantics? 

Dynamic allocation: 
	What is heap, what are other memory spaces? Text, data, bss and kernel space 

	Is allocation fast or slow?  - slower than stack 
	
Global variables:
	What are function bound global variables? 
		When are these initialized - data  section 
		When they are destroyed
		Are they thread safe
