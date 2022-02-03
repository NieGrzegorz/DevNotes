# Static assertion

Assertion evaluated in compile time. 

“The constant expression is evaluated at compile time and compared to zero. If it compares equal to zero, a compile-time error occurs and the compiler must display message (if provided) as part of the error message.

Otherwise, if expression does not equal zero, nothing happens; no code is emitted.

## Tips 
P.5: Prefer compile-time checking to run-time checking

T.150: Check that a class matches a concept using static_assert