Variables 
Python is dynamically typed, no explicit type is required in variable declaration 

multiply a string - concatenate a string with itself x times 

Python first creates value and stores it and then it assigns it to a variable 
a = 21 

21 is created first 


String formating: 

f-strings: 
strg = "Greg"

strg2 = f"Hi {strg}"  - embbedd the var in string 
.lower() // lower case string 

formated string template:

strg = "Greg"
greeting = "Hello, {}"
formated = greeting.format(strg)

it can be used with multiple placeholders 

strg = "something {} {} {}"
strg.format("pl1", "pl2", "pl3")


User input: 
name = input("prompt") 
It reads string - it needs casting: 

inp  = input("Give number") // string 
inp = int(inp) // integer

Booleans: 

is - keyword checks if the vars are exactly the same thing (the same memory space)


Function - callable variable in python 


lambda // unnamed function always used to return values 

add = lambda x, y: x + y // returns x+y 

in place called lambda: 
(lambda x,y: x+y)(5, 6)

map(function, collection) // call function on every item in collection 
but list comprehension is better and faster than map 
function in map can be lambda but we need to  cast return oof map to a list


Unpacking arguments:  variadic functions 

def multiply(*args): 	// arguments will be changed into a tuple of arguments 
	print(args) // prints tuple 
	
	
pass dict to 2 param fun 

def foo(x, y )
dict = {} // 2 elemt 

foo(**dict)

* = unpack operator 

Unpacking keyword arguments: 
def named(**kwargs): 
	print(kwargs) // dictionary
	
named(name = "Bob", age = 21)


type hinting: explicitly hint a type: 


def foo(sequence: list) -> float: 
// hint that arg should be list and should return a floating point value 

Imports: 
import -file- // import everything from a file 
from --file-- import --thing-- // import --thing-- from a file 

import sys 
sys.path - paths from which python can import

retlative imports: 


Errors in python: 
	raise ErrorName() // creating exception object  
	
catching: 
try: 
	//code to cry 
except ErrorName as e: // e is the instance of the exception ('as e part ' is optional) 
	//error handling code 
	
comon errors
TypeError ValueError RuntimeError 

you can add else: after except: 
and finally: 
there can be multiple except clauses 
	

Custom error classes :
class CustomError(ValueError): 
	// code 
	
custom error class must inherit from other exception (Exception or ValueError for instance)

First-class functions: Function that is just a variable that can be passed

Decorators: 

def decorator_func(func): 
	def decorate(): 
		//code 
		
	return decorate

function = decorator_func(function)
Decorator decorates existing function, replaces it 

"at" syntax:  // Instead of assigning a function a new value 

@decorator_func  // decorates 
def function: 
	//code 

functools 

@functools.wraps(functions) // keeps name for decorated function IMPORTANT 

Decorating functions with params: 

add *args, **kwargs  
as  param to replacing function** 

Decorator with parameters : 
	// add another level of decorator 


Mutability in python: 

Dont use mutable default parameter values 