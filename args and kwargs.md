args and kwargs can solve a whole lot of problems while passing data into the function.


```python 
class example:
    def __init__(self,*args,**kwargs):
        self.name = args[0]
        self.age = args[1]
        self.gender = args[2]

  

    def say(self):
        print("Hello my name is",self.name,"and my age is",self.age,"and my gender is",self.gender)

  

e = example("Mayan",20,"Male")
e.say()
```

this is a very good usage of args. This will help to make the function along the way of thinking.

now, in some case we might also use kwargs to pass specific.
