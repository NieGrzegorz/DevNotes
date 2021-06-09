# Dynamic linking and shared libraries
   

Dynamic link libraries (DLLs) are system libraries that are linked to programs at run-time. Dynamic linking is similar to dynamic loading.

The featur is commonly used with system libraries such as standard C lib. Using system libraries as static libraries increases the size of binary file and wastes the memory. D

Second advantage of DLLS is that libs can be shared among multiple processes that is why DLLS are also called SHARED LIBRARIES.

If the program references a routine that is in DLL, the loader locates the dll and loades it into memory if needed.

Dynamic llinking and shared libraries require help of OS. If the memory is protected, only OS can check whether the needed toutine is in another process memory space or OS can allow multiple processes acces the same moemory addresses.