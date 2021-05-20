[[Contents - START HERE]]

Interview questions with links to pages which answer these questions or answers for a specific questions. 

### Cpp General questions
1. [[Pointers and references#Pointer vs Reference|What are the differences between references and pointers in C++? ]]
2. What is a virtual function?  
3. What is early dispatch, early binding and late binding?
4. Can we delete this? 
	Yes, we can delete this
5. Can we call destructor explicitly?  - Yes 
7. [[Polymorphism|What are VTABLE and VPTR]]? 
8. [[Encapsulation#Access specifiers|What are Access specifiers in C++ ]]?
9. What are major C++ features? 
	Generic programming - templates 
	OOP paradigm 	
10. [[Manual memory allocation#C memory allocation vs C-style memory allocation| What is the difference between malloc/free and new/delete]]
11. [[Manual memory allocation#Free Store vs Heap|What is a difference between Free Store and Heap?]] 
12. [[Functions#What happens during a function call|What happens during a function call?]]
13. [[Functions#What is an Inline Function|What is an Inline function?]] 
14. [[Functions#Inline function vs Macro| What is the difference between inline function and Macro?]]
15. [[Friendship|What is a friend class and a friend function in C++?]]

16. Operator overloadng
	- Giving special meaning to user defined type 

17. Function overloading vs operator overloading 
	- Overloading having functions with the same name but different parameters 
	- Different types of arguments or different number of arguments 

18. [[Classes and objects#Constructors|What are types of constructors?]]
19. [[Inheritance|What is an inheritance?]] 
20. [[Static fields|What is a static keyword?]]
21. [[Namespaces|What is a namespace?]] 
22. What is a template?
	- generic type in C++ 
	- We may have genric classes and methods 

23. What is a lambda expression?
	- unnamed function 
	- Beneth - a class is generated with overloaded operator () 


23. Is there a garbage collecting mechanism in C++? 
	- So called smart pointers 
	- They release memory 
	- They allocate memory on free store 

24. What does std::move do? 
	- Rvalue cast 

25. What happens when C++ program is executed ? 
	- https://stackoverflow.com/questions/1204078/what-happens-when-you-run-a-program

26. Difference between static and dynamic library ? 
	- Static library - linked in compiletime 
	- dynamic library - linked in runtime 

27. Compilation vs linking 
	- Compilation process 

28. Functor: 
	- Function object 
	- Class which has overloaded operator () 
	- Customizable, may contain states 
	- You may pass functors to algorithms (std::transform) 

17. What is std::unique_ptr and std::shared_ptr and how they are used? 
19. What is RAII?
20. What is Undefined Behavior?
21. What is Linkage?
22. How to enable warning on gcc/clang/msvc?
23. How are template functions represented in the virtual table?
24. What is 0/3/5 constructor rule?
25. What is a borrowing system? 
26. What is constexpr?
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


What is a functor?
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
