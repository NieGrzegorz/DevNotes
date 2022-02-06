# Default and deleted functions 
## Default functions 
A more elegant, efficient way to provide a default implementation of a function, such as a constructor

## Deleted functions 
 A more elegant, efficient way to provide a deleted implementation of a function. Useful for preventing copies on objects.
 
 ## Syntax 
 
 ```C++ 
class Controller 
{
	public:
		Controller() = default; 	// Explicitly mark as default
		explicit Controller(unsigned int identifier); 
	
		// Prevent copy operations 
		Controller(const Controller&) = delete; 
		Controller& operator=(const Controller& copy) = delete; 
	
		// Prevent move operations 
		Controller(const Controller&&) = delete; 
		Controller& operator=(const Controller&) = delete;
};
 ```
 ## Tips 
 EMC++ Punkt 11:  Preferuj funkcje usunięte zamiast prywatnych niezdefiniowanych
Wyjaśnienie: 
-   Chodzi o automatycznie generowane funkcje składowe (konstruktory, operatory przypisania)
-   W C++ 98 żeby zapobiec kopiowaniu, deklarowało się je jako prywatne
-   Bardziej eleganckim rozwiązaniem jest zadeklarowanie ich jako funkcje usunięte 
-   Dodatkowo, można deklarować niechciane przeciążenia funkcji żeby zapobiec niejawnym konwersjom