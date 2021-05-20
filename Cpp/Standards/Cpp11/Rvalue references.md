# Rvalue references 
One of the [[C++11 Language features]]. 

### Rvalue references and move constructors:

-   Before C++11, rvalues (temporaries) were intended to not be modified (like in C), they were indistinguishable from const T& types. But in some cases they could be modified.
-   In C++11 new rvalue reference has been introduced, identified by T&&, it permits rvalues to be modified after their initialization for purpose of move semantics.
-   Problem with C++ 03 i is costly and uneeded deep copies that can happen implicitly when objects are passed by value.
-   In C++ 11

### Rvalues vs Lvalues:

T& - lvalue

T&& - rvalue

### Tags: 
#cpp11