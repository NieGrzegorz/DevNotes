Methods in class should take "self " as a first param 

def __init__(self): // constructor 

object.method() is a sytctic sugar for:
Class.Method(object)


Magic methods: because python calles them automatically 

__str__:  - define behavior of printing, the string representation of the object
this method must return a string 

__repr__: 
return to recreate the object quickly 
return string 

obj!r - calls repr method

istance method - every method in class that take "self" as a first param; called instnce method becose it needs object to call it (instance) 
used for most things, regular member function/method

@classmethod // takes class itself, uses class info but not object info 

@classmethod
def class_method(cls): 
call : Class.class_method() 

used often for factories 

@staticmethod // defines static method, free function inside a class, does not use class or object info

@staticmethod
def static_method(): // no param 

used just to place method in a class because it is related but does not use object or class, as in namespace 

Inheritance: 

class Derived(Base): 
	super()_init__() - call constructio of the base

Class composition: // build classes that use other classes 