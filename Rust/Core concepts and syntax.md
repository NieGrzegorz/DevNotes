# Core concepts and syntax 


## Variables 
Variables by default are immutable! If you want a mutable variable you need to be explicit about it. 
```Rust 
let x = 5; // Immutable 
x = 7; // Error 

let mut y = 5; // Mutable => conveys intent 
y = 6; // OK 

```

### Constant vs immutable 
- You are not allowed to use mut with constants - constants are always immutable 
- To declare constant use const instead of let 
- Type must be annotated in case of constant 
- Constant can be declared in any scope including glocal scope 
- Constants may be set only to constant expression, not to a result computed at runtime 
- Rust convention: upercase seperated with underscores name for constant 
- Constants are computed at compiletime (as contexpr in cpp)

### Shadowing 
Reuse the variable name -> new variable is created. Can use to shadow immutable vars or to change type.


## Data Types 
Rust is statistically typed -> type must be known at a compile time. 
There are two subsets of data types -> scalar and compound.
### Scalar types in Rust 
#### Integer
```Rust
// signed: i8, i16, i32 i64, i128, isize
// unsigned: u8, u16, u32, u64, u128, usize
let a: isize = 1; // signed, arch dependent 
let b: u8 = 1; // unsigned 8-bit  

```
Overflow : in debug mode -> panic! will happen at runtime. 
in release mode -> no checks are performed, two's complement wrapping will happen (256 will become 0 for u8 and 257 will become 1). Program won't panic. 

Handling overflow: 
"To explicitly handle the possibility of overflow, you can use these families of methods provided by the standard library for primitive numeric types:

-   Wrap in all modes with the `wrapping_*` methods, such as `wrapping_add`
-   Return the `None` value if there is overflow with the `checked_*` methods
-   Return the value and a boolean indicating whether there was overflow with the `overflowing_*` methods
-   Saturate at the value’s minimum or maximum values with `saturating_*` methods"

#### Floating-Point 
```Rust
let x = 2.0 // f64 
let y: f32 = 1.9 // f32 
```
#### Boolean 
```Rust
let x = true; 
let y: bool = false; 
```
####  Character type 
Char is four bytes. Represents Unicode Scalar Value. 
```Rust
let x = 'b'; 
let y: char = 'c'; 
```

### Compound types in Rust 
Types grouping multiple values. 

#### Tuple 
Fixed length, cannot grow or shirnk in size.  Can group different types. 
```Rust
let tup: (i32, f64, u8) = (500, 1.2, 1); // explicit types 
let (a, b, c) = tup; // decompose (destructing) a tuple into separate variables 

let first = tup.0; // access the first element of a tuple

```

The tuple without any values has a special name, _unit_. This value and its corresponding type are both written `()` and represent an empty value or an empty return type. Expressions implicitly return the unit value if they don’t return any other value.

#### Array 
Array elements must be the same type. Arrays have a fixed length. 
- Usefull if you want your data allocated on the stack and not on the heap
```Rust
let a = [0, 1, 2, 3, 4]; // array
let b: [u8; 2] = [1, 2]; // array of 2 elements of u8 type 
let c = [0; 5]; // array initialized with 5 zeros 
let first = a[0]; // access an element 
```


## Functions 
What a function is everyone sees. 
- Convention - snake case for function name 
- Signature MUST declare type of param 
- Return value in rust is synonymous with last expression in the function block 

```Rust
fn main() {

}

fn foo(x: i32) { // param of type i32 

}

fn five() -> i32 { // functions that returns 5 of type i32
	5
}

// To return value dont use ';'/ Semicolon makes the expression a statement and an error will occur
```

### Statement vs Expression
- Statement is an instruction that perform an action and does not return a value 
- Expression evaluate to a resulting value 
- Rust is expression-based language 
- If you add semicolon at the end of expression it makes it a statement

```Rust
let y = 6; //statement 

let x = {
	let b = 2; 
	b + 1
} // block is an expression , returns 3
```
## Control flow 

