# Final specifier 
Specifies that a virtual function cannot be overridden in a derived class or that a class cannot be inherited from.

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

class AnimatedImage: public Image
{
    public:
	    void setPosition() final; 
};
```
## Tips 
C.128: Virtual functions should specify exactly one of virtual, override, or final
C.139: Use final on classes sparingly