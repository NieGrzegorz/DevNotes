# Move semantics 

One of [[C++11 Language features]]. 


Main idea is to transfer ownership of objects from one object instance to another.

It enables to create move constructor and move assignment operator.

Move constructor:

class A

{

 // Move constructor

 A(A&& tmp);

}

Tags: 
#cpp11