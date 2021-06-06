# Functions 
One of the [[Basic features| basic features]] of C++ language. 

### Passing arguments
Function consists of a return type, function name, and argument list. C++ allows to pass arguments to functions in three different ways. 

#### Pass by value
#### Pass by pointer
#### Pass by reference 

### Function overloading

### What happens during a function call
* Cpu stores the memory address which called the function (to return to the caller)
* Copies arguments of a function to the stack (choosing proper calling convention)
* CPU transfers control to a fuction
* CPU executes the function code
* Returns control to the caller

### What is an Inline Function
* When function is succesfully inlined, body of the function is inserted at compile time
* A request, it is not 100% sure that function will be inlined 
* Good to use with small simple functions which are used often- to avoid overhead 
* In small functions overhead takes more time than executing the function

#### Benefits of inline functions: 
* Function call overhead will not occur
* Stack pushing/poping overhead will be eliminated

#### Disadvantages of inline functions:  
* Additional use of registers
* May increase compilation time
* Code size increases, generated binaries are bigger - this can be bad for embedded projects where binary size matters. 
	
### Inline function vs Macro 
* Macros should not be used in modern C++. In fact C++ code should eliminate preprocessor use as much as possible. 
* Macros cannot access private members
* With macros compiler doesn't do type checking

#### What is faster? 


### Tags: 
#cppbasic