```python
# A simple function that takes two numbers a, b and adds them
def add(a, b)
	return a + b

# define a tuple containing the argument values
values = (1, 2)

# ERROR - values is a single entity, so only one argument is passed here
add(values) 

# unpack the tuple with *
# this unpacks the elements of the tuple into positional arguments
# (1, 2) becomes 1, 2
add(*values)
```

