# nullptr
-   nullptr is a keyword 
-   nullptr is a pointer literal 
-   it is a prvalue of type std::nullptr_t (Address of an rvalue cannot be taken by built-in address-of operator)

## Tips 
- ES.47: Use nullptr rather than 0 or NULL
- EMC++ Punkt 8: Preferuj nullptr zamiast 0 i NULL. 
- EMC++ Punkt 8: Unikaj przeciążania typów całkowitoliczbowych i wskaźnikowych. 

0 to int i nie jest wskaźnikiem 
NULL - typ zależy od implementacji (może być int lub long) ale nie jest wskaźnikiem

## Further reading 
[Prvalue and other value categories](https://en.cppreference.com/w/cpp/language/value_category)