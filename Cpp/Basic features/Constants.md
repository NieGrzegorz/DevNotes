# Constants 
There are two types of constant values in C++: 
* [[Constants#constexpr|constexpr]] (since C++11)
* [[Constants#const|const]]

## constexpr
The **constexpr** specifier declares that it is possible to evaluate the value of the function or variable at **compile time**. Such variables and functions can then be used where only compile time constant expressions are allowed (provided that appropriate function arguments are given).

### constexpr variable 
-   LiteralType (known at compile time)
-   Must be initialized 
-   Initialization expression must be a constant expression
-   Class member variable must be static

### constexpr function 
A constexpr function must satisfy the following requirements:
-   its return type (if any) must be a LiteralType
-   each of its parameters must be a LiteralType
-   for constructor and destructor (since C++20), the class must have no virtual base classes
-   there exists at least one set of argument values such that an invocation of the function could be an evaluated subexpression of a core constant expression (for constructors, use in a constant initializer is sufficient) (since C++14). No diagnostic is required for a violation of this bullet.
-   it must not be [[Polymorphism#Virtual member functions|virtual]]
-   it must not be a coroutine

#### Constexpr function constriants in C++11
The function body can only contain:
-   null statements (plain semicolons)
-   static_assert declarations
-   typedef declarations and alias declarations that do not define classes or enumerations
-   using declarations
-   using directives
-   exactly one return statement

#### Constexpr function constriants in C++14
The function body may contain anything but:
-   an asm declaration
-   a goto statement   
-   a statement with a label other than case and default 
-   a try-block
-   a definition of a variable of non-literal type
-   a definition of a variable of static or thread storage duration 
-   a definition of a variable for which no initialization is performed

### constexpr class 
Class which has constexpr constructor 
Class becomes LiteralType

## constexpr vs const
[[Constants#const|const]] - declares an object as constant. This implies a guarantee that once initialized, the value of that object won't change, and the compiler can make use of this fact for optimizations. It also helps prevent the programmer from writing code that modifies objects that were not meant to be modified after initialization

[[Constants#constexpr|constexpr]] - declares an object as fit for use in what **the Standard** calls [[Constants#Constant expression|constant expressions]]. But note that constexpr is not the only way to do this.

## Constant expression
-   It can be used in places that require compile-time evaluation, for example, template parameters and array-size specifiers
-   Declaring something as constexpr does not necessarily guarantee that it will be evaluated at compile time. It can be used for such, but it can be used in other places that are evaluated at run-time, as well.
- An object may be fit for use in constant expressions without being declared constexpr.

## const
Keywod **const**  means roughly that this should not change after assignment. 

#### const function arguments
Marking function arguments as **const** prevents modyfing the arguments by the function itself. The entire check is done in compile time. 	

#### const references 
#### const functions 
We can make const a whole member function which means that the funciton does not modify the state of an object. It does modify **this** pointer. 

#### functions returning const


### Tags:
#cppbasic