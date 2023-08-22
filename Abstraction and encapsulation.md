A function is a piece of code that is executed when called.

IN REAL LIFE CODING, while using frameworks and libraries we don't give a Duck about the code that is written inside the function. We Straight away use it. This using the code inside the class and a function without worrying about the internal code is **Abstraction**.

### Encapsulation 

In real life, we keep some data private while some public. Same in software we can chose to keep some data private and some public. 

so to create a private attribute, here is how we do

```python 

class example:
	def __init__(self,at1 , at2):
		self.at1 = at1 
		self.__at2 = at2 
	def __str__():
		print("this is an example class")

obj = Example(10, 1000)

```


here `at2` is private and cannot be accessed outside because we added two underscore in `self.__at2 = at2` 

here is an example code and this what happens when you try to access a private data by mistake

```python 
class Customer:
    def __init__(self, cust_id, name, age, wallet_balance):
        self.cust_id = cust_id
        self.name = name
        self.age = age
        self.__wallet_balance = wallet_balance

c1=Customer(100, "Gopal", 24, 1000)
print(c1.__wallet_balance)

```

output 

```
Runtime Exception  
Traceback (most recent call last):  
File "file.py", line 16, in <module>  
print(c1.__wallet_balance)  
AttributeError: 'Customer' object has no attribute '__wallet_balance'
```

## but you can still access it with functions 

code 

```python 
class Customer:
    def __init__(self, cust_id, name, age,wallet_balance):
        self.cust_id = cust_id
        self.name = name
        self.age = age
        self.__wallet_balance = wallet_balance

    def update_balance(self, amount):
        if amount < 1000 and amount> 0:
            self.__wallet_balance += amount

    def show_balance(self):
        print ("The balance is ",self.__wallet_balance)

c1=Customer(100, "Gopal", 24, 1000)
c1._Customer__wallet_balance = 10000000000
c1.show_balance()

```

output 

```
The balance is 10000000000
```

### so why do we even make them private when we can access them outside with functions 

look in languages like java and c++ this is prohibited but in python you can do it.

It is like a warning to the developer , that this variable has nothing to be worried about and used with caution but the developer can use it when required. Something like the radioactive hazardous sign on packet of uranium.
