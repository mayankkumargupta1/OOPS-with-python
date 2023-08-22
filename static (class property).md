in some scenarios, we can't just change can't change the attributes of all the objects. 

because the objects that are been created might get missed and also that is not a very convenient method.

so we need a type of data that is static for all the objects and can be altered all the time depending on the situation.

here is an example how a static variable look like:

```python 
class example:
	I_am_static = "yo wassup"   # a static variable 
	def __init__(self,imp1,imp2):
		self.imp1 = imp1
		self.__imp2 = imp2
```

### how to access a static variable 

we can access the static variable with the help of the class , static belongs to the class not to the object.

here is an example 

```python 
class Example:
	i_am_static = "I am permanent"
	def __init__(self,at1,at2):
		self.at1 = at1 
		self.at2 = at2 
	
	def print_static(self):
		print(Example.i_am_static)


obj = Example(10,20)
obj.print_static()

Example.i_am_static = "Nah bro, i am"
obj.print_static()
```

self cannot change or access the static class variable.

### private static 

yes, we need it sometimes and therefore we can make it private variable by adding  `__` at the starting 

for example :

```python 

class Example:
	__your_crush_name = "A girl"
	def __init__(self,at1):
		self.at1 = at1 

	def get_static(self):
		return Example.__your_crush_name
	def set_static(self,name):
		Example.__your_crush_name = name

obj = Example('at1')

print("My previous crush is",obj.get_static())

obj.set_static("Money")
print("My current crush is",obj.get_static())
```


### we can also create static method and access the same way we access static variables :D
