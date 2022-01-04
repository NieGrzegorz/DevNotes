Lists: 

l = ["Greg", "Rolf"]
functions: 
.append(element) - add at the end 
.remove(element)

Tuples: // Cannot be modified 
t = ("Greg", "Rolf") // immutable 
t = 15, // tuple with single element

Sets:
s = {"Bob", "Rolf"} // cannot have duplicates in set
s = set() // crate empty set 
functions: 
.add(element)
call_set.difference(input_set) - calculates the difference set of call_set et and input_set
.union(input_set) - merges two sets 
.intersection(set) - common elements of two sets 
.symmetric_difference

List and tuples keep the order of elements
In set the order is not maitained 

subscript notation to access" 
l[0]
t[1]

Cannot use subscript the subscript notation 

List comprehension - create list on the fly from existing lists: 
numbers = [1, 2, 3]
double = [x * 2 for x in numbers ]

what you want to do (x * 2 ) for variable(x) in collection (in numbers)

additional filter at the end (if statement): 

evens = [x for x in numbers if x%2 == 0]

when you use list comprehension a new list is created 

Dictionaries:  // store key-value elements 

di = {"Key": 1, "Key2": 33}

// Key can be string int any other hashable type 
di["Key"] // access value from dict 

di["Kay3"] = 22 // add new or modify key 

List of dictonaries: 

friends = [
	{"name":"Bob", "age": 11} 
	{"name":"Adam", "age": 31}
]

friend[0]["name"] // "Bob"

for loop gets Keys 
for key, value in di.items(): 
	// do something
	
Can check if key exists with "in" keyword
.values() - get just values 

Destructuring variables : 
x, y = 5, 8 // x is 5 and y = 8

t = 3, 4
y, a = t //destructured

Key- val pair in dictionary is a tuple 

use underscore to ignore variable - just convention 
t = ("bob", 1, "sth")
name, _, str = t

head, *tail = [1, 2, 3, 4,5] // head - 1 tail - rest
*head, tail = [1, 2, 3,4 ,6] // tail - 6, head -  rest 


Dictionaryy comprehensions: 
user_dict = {user[1]: user for in users}