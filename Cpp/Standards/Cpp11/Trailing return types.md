# Trailing return type

An alternative way to indicate the return type. 
``` C++

auto foo() -> int
{
	return 0; 
}

template <typename T, typename U> 
auto foo(T a, U b) -> decltype(a + b)
{
	return a + b; 
}

int main() 
{
	auto l = []() -> int {return 1;};
	return 0; 
}
```

## Usage 
- Automatic deduction of return type in templates
- The only way to explicitly show the return type of lambda  