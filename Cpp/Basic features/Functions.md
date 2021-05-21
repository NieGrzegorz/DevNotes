# Functions 

### Passing arguments
#### Pass by value
#### Pass by pointer
#### Pass by reference 

### Function overloading

### What happens during a function call
	- cpu stores the memory address which called
	- copies arguments to stack
	- and transfers control to a fuction
	- executes the function code
	- Returns control to the caller

### What is an Inline Function
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
	
### Inline function vs Macro 
	- Macros should not be used 
	- Macros cannot access private members
	- With macros compiler doesn't do type checking


### Tags: 
#cppbasic