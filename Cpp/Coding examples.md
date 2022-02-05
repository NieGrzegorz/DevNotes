# Coding examples 


### Replace char in std::string with another string
```C++

std::string str = "Text to replace.";
std::string to_replace = "."; 
std::string pattern_insert = "text"; 
int pos; 

while((pos = str.find(to_replace, pos)) != std::string::npos)
{
	str.replace(pos, to_replace.length(), pattern_insert);
	pos += pattern_insert.length(); 
}


```