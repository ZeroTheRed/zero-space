[Writing Python like it’s Rust | Kobzol’s blog](https://kobzol.github.io/rust/python/2023/05/20/writing-python-like-its-rust.html)
1. Use type hinting wherever possible to introduce strong typing and remove possibilities of the code being used incorrectly
	```python
- # argument: argument type, def func(args) -> return type
def calculate_hypotenuse(x: float, y: float) -> float:
	return sqrt(x**2 + y**2)

```
2. Use dataclasses for strongly typed interfacing and to show what the function is actually returning (both types and nature of content)
	```python
# dataclasses decorator @

@dataclasses.dataclass
class Person:    
	name: str
	age: int
	employed: bool

def find_person(...) -> Person:
	...
```
3. You can use `typing.Union()` or `dataclass1 | dataclass2 | ...` to unionize different types to enable efficient pattern matching