# Data Casting
Data casting means converting an expression of one type into another.

## Implicit data casting 

## Explicit data casting 
### static_cast
Static cast performs no runtime checks. Used to reverse an implicit cast. 

Static cast performs a conversion between compatibile types. It is like C-style cast but more restrictive. 

Usage -> integer types; compatibile pointers as casting from void* to a proper type. 

### dynamic_cast
This type of casting may be used only with pointers or references to objects. The purpose of this cast is to make sure that the result is a valid complete object of requested class. Dynamic cast provided **run-time checking** and requires **Run-Time Type Information (RTTI)**. Some compilers have this option disabled by default. 

dynamic_cast is used to cast an object of a class to one of its base classes. 

When class is a polymorphic class, dynamic_cast performs a special run-time check to be sure that we get a complete object. 

* If dynamic_cast cannot cast a pointer because it is not a complete object (like in casting base class into a derrived class), it returns a **nullptr**
* If dynamic_cast is used to convert a reference type and conversion is not possible, a **bad_cast** exception is thrown. 

### reinterpret_cast
Converts a pointer type to any other pointer type, even if classes are not related. 
The operation is a simple binary copy of a value from the pointer to another. No type checking is performed. 

It can cast pointers to integer types. The guarantee is that casted pointer will fit into integer type and it can be cast back into a valid pointer. 

### const_cast
Manipulates with the constness of an object. It sets the value const or removes const. 

### any_cast (C++17)

### C-style cast (Legacy)