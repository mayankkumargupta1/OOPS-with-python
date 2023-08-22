what would happen if we pass an object into parameters.

here is what will happen 

```python 
class Example:
    def __init__(self,num):
        self.number = num 
    def __str__(self):
	    print("an example class")

def change_number(new_self):
    new_self.number = 100 

obj = Example(10)
print(obj.number)

change_number(obj)
print(obj.number)
```

output 

```
10
100
```

you guess right when we pass object as a parameter, the parameter becomes a reference variable to self. 

