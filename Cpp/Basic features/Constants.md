# Constants 

There are two types of constant values in C++: 
* constexpr
* const

### constexpr
The expression which is marked **constexpr** must be known at compile time

### const
Keywod **const**  means roughly that this should not change after assignment. 

#### const function arguments
Marking function arguments as **const** prevents modyfing the arguments by the function itself. The entire check is done in compile time. 	

#### const references 
#### const functions 
We can make const a whole member function which means that the funciton does not modify the state of an object. It does modify **this** pointer. 

#### functions returning const

### Tags:
#cppbasic