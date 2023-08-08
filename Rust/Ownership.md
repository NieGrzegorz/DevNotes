# Ownership 
Mechanism to manage memory in Rust

## Ownership rules
- Each value has its owner 
- There can be one owner at a time 
- When owner goes out of scope the value is dropped 

## Memory management 
In rust, memory allocated is freed when a variable goes out of scope. 
Rust calls automatically a function called ``drop``. Called automatically at closing curly bracket (equivalent to RAII in cpp). 

```Rust
let s1 = String::from("hello"); 
let s2 = s1; // Moved! s1 is now not available 
	
// Rust does not make deep copy automatically 
// To make deep copy: 
let s3 = s2.clone(); 
```

## Ownership and functions 

## References - borrowing 
Passing by reference does not copy and it does not transfer ownership. 
Passing by reference is called borrowing since the instance is borrowed and we do not need to transfer the ownership back. 

Passing by reference is immutable by default. Reference must be explicitly marked as mut to modify the object pointed by the reference. 

## Slice type 


