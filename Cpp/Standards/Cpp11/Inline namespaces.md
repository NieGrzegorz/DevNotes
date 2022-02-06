# Inline namespace 
Declarations inside inline namespace will be visible in its enclosing namespace.

Bjarne: 
“The inline namespace mechanism is intended to support library evolution by providing a mechanism that support a form of versioning.(...)The point is that the inline specifier makes the declarations from the nested namespace appear exactly as if they had been declared in the enclosing namespace.”

[Inline namespace](https://www.stroustrup.com/C++11FAQ.html#inline-namespace)

## Usage
```C++
//file V99.h:
inline namespace V99 {
	void f(int);	//** does something better than the V98 version **
	void f(double);	//** new feature 

//file V98.h:
namespace V98 {
		void f(int);	//** does something 
}

	//** file Mine.h: **
namespace Mine {
	#include "V99.h"
	#include "V98.h"
}



#include "Mine.h"
using namespace Mine;
V98::f(1);	//** old version **
V99::f(1);	//** new version **
f(1);		//** default version
```