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

## Traps 

## How does it work under the hood? 
