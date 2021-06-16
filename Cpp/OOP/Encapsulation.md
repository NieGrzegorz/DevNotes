# Encapsulation

Encapsulation is one of four pillars of [[OOP| Object Oriented programming]]. The main rule of encapsulation is to "Keep your things private". Do not expose member variables of a class to the outside. Member variables should be private and accessible (if needed) by well defined public methods.

### Access specifiers
To enable make encapsulation possible, C++ introduces three access specifiers which may be used in structs and classes: 
* private -> members are accessible from inside the class, it is not exhibited. 
* public -> members are accessible outside the class.  
* protected -> members are accessible inside the class and in classes inheriting from this one.  

### Benefits:  
* We can trace on call stack that setter was called. If some code modifies member variable directly, it cannot be traced. 
* Defining public interface of a class which can be used by other code leads to well structured code. 

