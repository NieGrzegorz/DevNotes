# Inline namespace 
Declarations inside inline namespace will be visible in its enclosing namespace.

Bjarne: 
“The inline namespace mechanism is intended to support library evolution by providing a mechanism that support a form of versioning.(...)The point is that the inline specifier makes the declarations from the nested namespace appear exactly as if they had been declared in the enclosing namespace.”

[Inline namespace](https://www.stroustrup.com/C++11FAQ.html#inline-namespace)