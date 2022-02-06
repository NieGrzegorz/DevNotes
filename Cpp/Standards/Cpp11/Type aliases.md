# Type aliases 
An alternative way of referring to an object; often a name, pointer, or reference. 

Semantically similar to using a typedef however, type aliases with using are easier to read and are compatible with templates.

## Examples 
### Templated alias 
```C++

template <typename T> 
using Cache = std::vector<std::shared_ptr<T>>; 

int main()
{
	Cache<Gui::Screen> screenCache; 
	return 0; 
}
```

## Tips 
T.43: Prefer using over typedef for defining aliases. 

T.42: Use template aliases to simplify notation and hide implementation detail

EMC++ Punkt 9: Preferuj deklarację aliasów zamiast typedef