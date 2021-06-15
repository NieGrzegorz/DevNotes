# Exceptions
Mechanism to  handling errors in software. 


### What is an exception 
* A function that cannot cope with a problem *throws* an exception 
* A function that wants to handle a kind of problem *catches* an exception
* Exception means that some  part of the system couldn't perform what it was asked to do


### Exception handling mechanism 
* Is an alternative to the traditional techniques which are inelegant and error prone 
* Allows to separate error-handling code from "ordinary" code. Code is more readable 
* Unifies the error handlig style 


### Legacy error handling techniques 
* Terminate the program 
* Return an arbitrary *error value*
* Return legal value but leave the program in *error state*. The example in C standard library is that some functions set the nonlocal variable *errno* to indicate an error
* Call an error-handler function 


### What happens when an exception is thrown
Ultimate response to an unhandled error (*uncaught excetption*) is to terminate the program. Where termination is unacceptable, we can catch all exceptions. Exception terminates the program as long as developer allows it to terminate. 

When termination is acceptable response to an error, an uncaught exception will achieve it by calling **terminate()**. Also [[Noexcept specifier]] can make it explicit.

### When not to use exceptions
* A time-critical embedded system where an operation must be guaranteed to complete in a specific maximum time. 
[[RAII]]