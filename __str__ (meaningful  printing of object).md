If we print an object, the output looks something like this 

```python 
class Example:
	def __init__(self, at1 , at2):
		self.at1 = at1 
		selft.at2 = at2 

obj = Example(20,30)

print(obj)
```

output
```
<__main__.Example object at 0x00000143FDC15570>
```

Now to make this look a little bit meaningful we use `__str__`  method to describe the class.
It certainly does not play any role in the development but is very useful in debugging.

Here is an Example code 

```python
class Example: 
	def __init__(self, at1 , at2):
		self.at1 = at1 
		self.at2 = at2 
	def __str__(self):
		return "This is an example class with two attributes " +str(self.at1)+" and "+str(self.at2)

obj = Example(10,20)
print(obj)
```

output

```
This is an example class with two attributes 10 and 20
```

