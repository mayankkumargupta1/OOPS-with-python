There are some of the most basic rules to define them and they are very easy to begin with.

here is a custom class in python 

```Python 
class Hellow:
	pass
```

now lets create an object of it

```python 
class Hellow:
	pass 

object = Hellow()
```

Here we have a new candle **(Object)** out of the mold **(Class)** 
Now to give this new object some of its own unique properties **(attributes)** , Here is the how we do that

```python 
object.wick = 'large'
object.smell = 'lavender'
object.length = 10 
```

so these are all the properties that I have specified for the new candle.

### Rules for creating one 

The Rules are very Simple creating an attribute name follows the same rule as creating a identifier in python.

### How to access them ?

that is also pretty easy 
just call them with the attribute 

```python 
print(object.length)
```

**output**
```
10
```

### Common and Easier way of creating attributes 

for doing so we create a special function called init. 

```python 
class Candle:
	def __init__(self, size, color):
		self.color = color         # defines attribute color
		self.size = size           # defines attribute size 	

#creating objects and assigning the respective values 
candle1 = Candle("red",10)         
Candle2 = Candle("green",20)
```

now lets understand the above init function 

```python
class new:
	def __init__(self):
		pass
```

the  above function you see in the class is called a [[constructor]].

And the word ``` self ```  you see here is not a keyword. It refers the the **Object** being executed.
