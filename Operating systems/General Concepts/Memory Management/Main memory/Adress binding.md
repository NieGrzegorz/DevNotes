# Adress binding 
Part of [[Basic information]] of memory management. 

### General information
Operating System normally allow the process to be anywhere in physical memory. A program normally goes through several steps before execution. Addresses in the program are represented differently duruing these steps. In source program the addresses are normally **SYMBOLIC**. **COMPILER** binds the **SYMBOLIC** adresses to **RELOCATABLE** addresses. 

Binding is a **MAPPING** from one address to another.

   
### When the address binding may occur? 
Binding of instructions and data to memory addresses can be done at any step along the way: 

* **Compile time** - if you can know at compile time where the process will reside in memory, then **absolute code** can be generated. You have to recompile if you want to change the starting location i memory.
* **Load time** - If it is not known at compile time where the process will reside, the compiler mus generate **RELOCATABLE CODE**. The binding to the memory is delatyed until the **LOAD TIME** of the process. Program has to be reloaded if starting address changes.
* **Execution time** - If the process can be moved around in memory during its execution, the binding is delayed untile the **RUN TIME**. Special hardware is needed for this (MMU). **MOST OS USE THIS METHOD**