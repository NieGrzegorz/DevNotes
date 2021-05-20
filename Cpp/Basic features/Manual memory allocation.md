# Manual memory allocation
One of [[Basic features]] of C++ language. 

### C++ memory allocation vs C-style memory allocation

New/delete: 
	Memory allocated from Free Store 
	Returns a fully typed pointer 
	new never returns null - it throws exception on failure 
	Has version to handle arrays 
	Can add a new memory allocator to deal with low memory (set_new_handler) 
	Can be overriden legally 
	Constructor/destructor is called 

malloc/free
	Memory allocated from heap 
	Returns a void* 
	Must specify the size required in bytes 
	Realocating larger chunk of memory is simple (no copy constructor) 
	They WONT call new/delete 


### Free Store vs Heap
Free Strore vs Heap: 
 - Free Store and heap are not interchangable 
 - They are separate concepts but they exist in the same memory region 
 - HEap is managed with malloc/free
 - Free store is managed with new/delete