A constructor helps to create predefined attributes for the class. 

here is an example of a constructor
```python 
class Example:
	def __init__(self, at1,at2):
		self.at1 = at1 
		self.at2 = at2 

obj = Example(10,20)
print(obj.at1)
print(obj.at2)
```

output
```python 

10
20
```

```__init__``` is the boiler plate function for creating a constructor and the 
self in ```__(self,at1,at2)```  refers to the object that is currently being executed. Other than that at1 and at2 are the identifiers. 

note attributes with constructor can only be created with self , without self we are just creating local variable .

### creating a function with self 

we can also create function with self, by just introducing the self parameter inside the parenthesis.

here is an example on how to do so. 

```python 
class example:
	def __init__(self, at1, at2):
		self.at1 = at1 
		self.at2 = at2 
	def A_brand_new_function(self):
		print("Boom")

obj = example(None,None)

obj.A_brand_new_function()
```


Output 
```
Boom
```

we can also use the value assigned to the attribute inside the function. Here is How

```python 
class Example:
	def __init__(self, atribute):
		self.atribute = atribute 
		
	def func(self):
		print(self.atribute)

obj = Example("Hellow")

obj.func()
```

Output 
```
Hellow 
```


----------- I got lazy 😁

![[Pasted image 20230718010625.png]]


### some crazy shit 

![[Pasted image 20230718011111.png]]

![[Pasted image 20230718011126.png]]

now let me explain this to myself real quick 

got it ,
I will explain this with a piece of code. Basically these examples justify that the function can only access the attributes with the self keyword. 

Note: we can use words other that self 

![[Pasted image 20230718012414.png]]

in this example I replaced self with fat, this is some witchcraft but yes it works. 

I guess the only reason it is here is to make everyone comfortable. 

