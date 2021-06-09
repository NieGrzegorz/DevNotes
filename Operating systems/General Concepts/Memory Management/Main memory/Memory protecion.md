# Memory protection 
  
The memory space for the process is defined. Two registers are used base register (holds the starting address) limit register (size of the range) \- handled by CPU not the OS. In case of violation CPU traps into the OS which treats it as fatal error.