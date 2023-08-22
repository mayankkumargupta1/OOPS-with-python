In Python, we Objects are like balloons and if we don't tie a ribbon, they escape.

The ribbon which us used to tie the balloon is called the reference variable.

we store the object and its properties in the reference variable.

here is an example 
```python 
class Example:
	def __init__(self,id):
		self.id = id 

Example(1220)                  # free balloon cannot be used again 

obj = Example(8982)            # Can be used again 
```