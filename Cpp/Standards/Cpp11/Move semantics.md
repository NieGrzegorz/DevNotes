# Move semantics 

One of [[C++11 Language features]]. 

## What is move semantics? 
Main idea is to transfer ownership of objects from one object instance to another.
It enables to create move constructor and move assignment operator.

## Move operations 
```C++
class Movable
{
	public: 
        // Move constructor
        A(A&& tmp);
};
```

Tags: 
#cpp11