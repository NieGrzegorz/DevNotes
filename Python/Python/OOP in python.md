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