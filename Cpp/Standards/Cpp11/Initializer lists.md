# Initializer list 

## General info 
- std::initializer_list was introduced in C++11
- located in \<initializer_list\> header
- object of type std::initializer_type\<T\> allows group initialization of elements of type T for a class which has a parametrized constructor which takes a std::initializer_list as a param 
- Compiler generates an object of this type when we use braced-init-list

```C++
std::vector<int> vec = {0, 1, 2, 3, 4};
```

## What happens when we create std::initializer_list 
- Temporary const array of length of elements in braced list is created which holds elements of a type T 
- Lifetime of the array is the same as the lifetime of std::initializer_list object 
- std::initializer_list does not hold the values from the array but only the pointers to the first and last element or pointer to the first elemet and the length of the array
- Copying std::initializer_list object causes two objects to point to the same memory 

## When std::initializer_list is created automatically 
- When braced-init-list is used to initialize an object of a class which has a parametrized constructor taking std::initializer_list as a param 
- When we use braced-init-list as right-hand operand of the assignment operator or we pass it as a function parameter if the operator or function take std::initializer_list as one of parameters 
- When braced-init-list is connected with auto in range-based for loops 