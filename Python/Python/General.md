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