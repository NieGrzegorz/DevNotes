# Explicit virtual overrides 
Specifies that a virtual function overrides another virtual function. If the virtual function does not override a parent's virtual function, throws a compiler error

```C++ 
class IWidget
{
	public: 
	    virtual void setPosition() = 0; 
};

class Image: public IWidget
{
    public: 
	    void setPosition() override; 
};
```

## Tips 
- C.128: Virtual functions should specify exactly one of virtual, override, or final
- EMC++ Punkt 12: Deklaruj funkcje nadpisujące jako override