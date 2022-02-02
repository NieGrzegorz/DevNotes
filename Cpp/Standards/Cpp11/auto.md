# auto 

## auto keyword in C language 

It's a storage class specifier, like static. It's basically the opposite of static when used on local variables and indicates that the variable's lifetime is equal to its scope (for example: when it goes out of scope it is automatically destroyed).

```C
{
 int Count;
 auto int Month;
}
```

## Keyword auto introduced in C++11 
 New meaning of  `auto` keyword. 
 
 It allows automatic type deduction on the basis of initializing expression and it allows for automatic type deduction for lambda parameters. It is also possible to define functions returning `auto`. 
 
Compiler evaluates the type on the basis of initializing expression. 
 
Examples of initializing expressions: 
 * `auto a { 42 };` (Universal initialization)  
 * `auto b = 0;` (Assignment)
 * `auto c = { 3.14156 };` (Universal assignment syntax)
 * `auto d( 1.41421f );` (Direct initialization, or constructor-style)
 
[source](https://docs.microsoft.com/en-us/cpp/cpp/auto-cpp?view=msvc-170)

## When to use? 
- Use as much as possible 
- Don't use only when you want to be explicit with a type of a variable 

## Traps 
- It is possible that some classes contain proxy classes and you get unexpected type

## How does it work under the hood? 

#### auto type deduction 
Template argument deduction is used in declarations of variables, when deducing the meaning of the auto specifier from the variable's initializer. 
The parameter P is obtained as follows: in T, the declared type of the variable that includes auto, every occurrence of auto is replaced with an imaginary type template parameter U or, if the initialization is copy-list-initialization, with `std::initializer_list<U>`. The argument A is the initializer expression. After deduction of U from P and A following the rules described above, the deduced U is substituted into P to get the actual variable type:
```CPP 
const auto& x = 1 + 2; // P = const U&, A = 1 + 2:
 // same rules as for calling f(1 + 2) where f is
 // template<class U> void f(const U& u)
 // deduced U = int, the type of x is const int&
auto l = {13}; // P = std::initializer_list<U>, A = {13}:
 // deduced U = int, the type of l is std::initializer_list<int>
```
In direct-list-initialization (but not in copy-list-initalization), when deducing the meaning of the auto from a braced-init-list, the braced-init-list must contain only one element, and the type of auto will be the type of that element:
```CPP 
auto x1 = {3}; // x1 is std::initializer_list<int>
auto x2{1, 2}; // error: not a single element
auto x3{3};    // x3 is int
 // (before N3922 x2 and x3 were both std::initializer_list<int>)
```
#### auto-returning functions (since C++11)
Template argument deduction is used in declarations of functions, when deducing the meaning of the auto specifier in the function's return type, from the return statement. 
For auto-returning functions, the parameter P is obtained as follows: in T, the declared return type of the function that includes auto, every occurrence of auto is replaced with an imaginary type template parameter U. The argument A is the expression of the return statement, and if the return statement has no operand, A is void(). After deduction of U from P and A following the rules described above, the deduced U is substituted into T to get the actual return type: 
```CPP
auto f() { return 42; } // P = auto, A = 42:
 // deduced U = int, the return type of f is int
```
If such function has multiple return statements, the deduction is performed for each return statement. All the resulting types must be the same and become the actual return type. 
If such function has no return statement, A is void() when deducing. 
Note: the meaning of decltype(auto) placeholder in variable and function declarations does not use template argument deduction. 
 
[source](https://en.cppreference.com/w/cpp/language/template_argument_deduction#Other_contexts)

****
