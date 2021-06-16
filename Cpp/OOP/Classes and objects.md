# Classes and objects 

### What is a class
### What is an object
### Constructors
Big topic so placed in a separate note: 
[[Constructors]]



### Destructor
A special type of method which is called when object is deleted. Destructor should not throw an exception during its call so should be marked as [[Noexcept specifier| Noexcept]]. 

#### Virtual destructor 
#### Can we call destructors explicitly? 

### "this" pointer
#### Can we delete "this" pointer? 
Yes - only when object is allocated on heap
Otherwise = runtime error


### Function objects (Functors)
	- Function object 
	- Class which has overloaded operator () 
	- Customizable, may contain states 
	- You may pass functors to algorithms (std::transform) 
	
### Polymorphic class 
- a class that defines or inherits at least one virtual function.

### Abstract class