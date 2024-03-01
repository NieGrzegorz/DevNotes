
Rust groups errors in two categories: 
*  Recoverable 
* Unrecoverable
## Unrecoverable errors with panic! 

There are two ways to cause panic: 
* Take an action that causes panic 
* Explicitly call panic! macro 

Panic by default: 
* Prints a failure message
* unwinds 
* clean up a stack 
* quits 

It is possible to set environment variable so Rust prints a stack  - set RUST_BACKTRACE=1

and the build must contain debug symbols (must be compiled without --release)

## Recoverable errors with Result

Result is defined as follows: 
```Rust
enum Result<T, E>  {
		Ok(T), // T is type of value returned in case of success
	Err(E),    // E is error type that is returned in case of error
}
```

### unwrap and expect 

Both methods are used to return value from Result if it is Ok and panic! when there is an error. 

### Propagating errors 