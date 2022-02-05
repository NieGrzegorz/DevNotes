# Lambdas 
One of [[C++11 Language features]]


## What is lambda? 
Lambda is an unnamed function object. It consists of :
-   Capture list
-   Optional set of parameters wit an optional trailing return type
-   Body

Caputre list:

``` C++
[](){}; // capture nothing
[=](){}; // capture local objects in scope by value (local variables, parameters)
[&](){}; // capture local objects in scope by reference (local variables, parameters)

[this](){}; // capture this pointer by value
[a, &b](){};  // capture objects a by value and b by reference
```

### Tricks 
Lambda as comparator in cpp17: 
```C++
std::set myset{{MyData{"Bob"}}, [](const auto &lhs, const auto &rhs){ 
	return lhs.key < rhs.key; 
}};
```

Explanation: We cannot use lambda type as template argument so we have to use a constructor of std::set which takes std::initializer_list and comparator
Lambda as comparator in cpp20:

### Tags: 
#cpp11