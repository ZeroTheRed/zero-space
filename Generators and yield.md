A <font style="color:#FF00FF">generator</font> is a one-time use iterator, an example of lazy evaluation because it does not consume memory.

`yield` suspends the function execution and returns its value to the caller. Used in generator functions.

```python
def generator():
	yield 1
	yield 2 
	yield 3

for x in generator():
	print(x)
```

