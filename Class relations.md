so far we have only interacted with class and objects.

can classes and objects interact with each other ?

yes they can.
but we make certain relationships to make interactions 
almost all the types of interaction is possible with these three relationships. 

![[Pasted image 20230803011430.png]]

## aggregation 

of a class A own class B then class A is called aggregate of class B, commonly known as has-A relationship.

here is an example:
![[Pasted image 20230803012756.png]]


__ continuing after 6 days __ 

look aggregation is very simple it is made difficult to understand 

Aggregation is like adding data access the authority class. You can identify this by using 'Has a' phrase.
for example : car has a driver, car has a ac, car has a paint, also you can take the example of a candle.
Candle has a wick, candle has a color, candle has a price. 

all the data like 
driver, ac, paint or wick, color, price 
can be stored in separate classes and use a parent class to access them like car and candle, instead of creating a very complex class.

here is a code to tell that in a very easy way.

```python 
  

class Candle:
    def __init__(self , price , wick , color ):
        self.color = color
        self.wick = wick
        self.__price = price
        
    def __str__(self):
        return str("this is a candle with color "+str(self.color)+" and wick with diameter "+str(self.wick.diameter)+" and stiffner "+str(self.wick.stiffner)+" with price "+str(self.__price.show_number())+" and discount "+str(self.__price.show_discount()))

    def show_price(self):
        return [self.__price.show_number(),self.__price.show_discount()]
    def change_price(self, new_price, new_discount):
        self.__price.change_number(new_price)
        self.__price.change_dicount(new_discount)

class color:
    def __init__(self,color_name: str, hex: str = None, rgb: tuple= None, cmyk: tuple = None, hsv: tuple = None, hsl: tuple = None):
        self.hex = hex
        self.rgb = rgb
        self.cmyk = cmyk
        self.hsv = hsv
        self.hsl = hsl
        self.color_name = color_name
    def __str__(self):
        return self.color_name

class wick:
    def __init__(self , diameter, stiffner):
        self.diameter = diameter
        self.stiffner = stiffner
    def __str__(self):
        print("this is a wick with diameter",self.diameter,"and stiffner",self.stiffner)    

  

class price
    def __init__(self , number , discount):
        self.__number = number
        self.__discount = discount

  

    def show_number(self):
        return self.__number
    def change_number(self,number):
        self.__number = number

  

    def show_discount(self):
        return self.__discount
    def change_discount(self,discount):
        self.__discount = discount

  

color = color(rgb=(184, 65, 15),cmyk=(0, 65, 92, 28),hex="#b8400f",hsl=(17, 85, 39),hsv=(17, 92, 72),color_name="Rust")
wick = wick(2,"copper")
price = price(300,5)
candle = Candle(price,wick,color)
print(candle)
```

here is an example for car  too 

```python 
class car:
    def __init__(self,driver,ac,color):
        self.__driver = driver
        self.ac = ac
        self.color = color

    def __str__(self):
        return "This is a car with driver " + str(self.__driver) + " and ac " + str(self.ac) + " and " + str(self.color)

    def access_driver_details(self):
        print(self.__driver)

    def change_driver_details(self, name, age, gender, country, experience):
        self.__driver.change_details(name = name, age = age, experience = experience, gender = gender, country = country)

  
  

class driver:
    def __init__(self, name, age, experience, gender, country):
        self.__name = name
        self.age = age
        self.experience = experience
        self.__gender = gender
        self.__country = country
  

    def __str__(self):
        return "name: " + str(self.__name) + " age: " + str(self.age) + " experience: " + str(self.experience) + " gender: " + str(self.__gender) + " country: " + str(self.__country)

    def access_name(self):
        return self.__name

    def access_gender(self):
        return self.__gender

    def access_country(self):
        return self.__country

    def change_details(self, name, age, experience, gender, country):
        self.__name = name
        self.age = age
        self.experience = experience
        self.__gender = gender
        self.__country = country

  

class color
    def __init__(self,color,hex):
        self.color = color
        self.hex = hex

    def __str__(self):
        return "color: " + str(self.color) + " hex: " + str(self.hex)

class ac:
    def __init__(self,type)
        self.type = type
    def __str__(self):
        return "type: " + str(self.type)

  

color = color("red","#ff0000")
ac = ac("premium")
driver = driver("mayank", 18, 4, "male", "India")

  
car = car(driver, ac, color)
print(car)
```

### dependency of static or local 

well some class relations can be a bit more complex like using a class to store data or to function it as a function. 

here is an example with local variable 

```Python 

class Static_class:
    static_variable = "some static data "

class Odin:

    def __init__(self,Your_name :str):
        self.Your_name = Your_name
    def __str__(self):
        return "hey "+self.Your_name+" your example class has "+Static_class.static_variable

obj = Odin("mayank")
print(obj)

```

output :

`hey mayank your example class has some static data `



### Inheritance

Inheritance is like creating a very common class and storing a bunch of common not so important data and then getting data out of that class to a group of important classes that are actually important and functional.

Inheritance is also called "is-A" Relation ship 

for inheritance to work we need to maintain a proper family tree of class .
the class that is inheriting the data is called a child class and the class that is being inherited is called a parent class.

here is an example of what I am talking about.

![[Pasted image 20230817174243.png]]

here you can see price, brand and camera are all common info so we stored it in a class called Phone.
In this case, class Phone is the parent class and the other classes called FeaturePhone and SmartPhone are child class. 

we can also confirm this by saying "phone is a FeaturePhone" and "phone is a SmartPhone"

Boom i got lazy 

![[Pasted image 20230817175113.png]]

*also you can inherit  freaking functions*

here is an example code for inheritance 
```python 

class phone:
	def __init__(self, price :int, discount :int, camera :str):
		self.price = price 
		self.discount = discount 
		self.camera = camera 
	def buy(self):
		print("buying")
	def return(self):
		print("returning")

class smart_phone(phone):               #inheriting phone
	pass
class featured_phone(phone):             #inheriting phone
	pass 

obj = featured_phone(50000,5, "dual camera ")
```

What properties can be inherited ?

now this is a very serious question because it is related to security of the application too

- constructor (all of them except if it does not have its own constructors)
- Methods

#### Method over riding 

Sometimes a child may not want to use what it has inherited from the parent. The same holds true for OOP as well. If the child class does not want to use a method inherited from the parent class then it may create its own method with the same name.

When the child has a method with the same name as that of the parent, it is said to override the parent’s method. This is called as **Method Overriding**. Method overriding is also called as **Polymorphism**.

_____ the above is copy pasted 

#### Use of super 

If class want to use any function from its parent class then it can use `super()` function.

here is a very nice example of super and method over riding 

```python 
class Example:
    def __init__(self,public :int,private :str):
        self.public = public
        self.__private = private

    def func(self):
        print("parent class function ")

  

class Example_child(Example):
    def func(self):
        print("Child class function ")
        super().func()

Example_child(5,"hello").func()
	
```

we can also inherit and super impose the attributes of inheriting class by using super function.

```python 
class Parent:
	def __init__(self,price :int, name :str):
		self.__price= price 
		self.name = name 
	def random_method(self):
		print(self.name, self.__price)

class child(Parent):
	def __init__(self,name :str, price :, extra_stuff)
		super().__init__(price, name)
		self.extra_stuff = extra_stuff 

```


#### Types of inheritance 

so these are all the main types of inheritance 

![[Pasted image 20230819184713.png]]

now in all of these the one that is by far most uncommon type is the **Multiple** inheritance.

what happens is in some cases like Odin in smart phones. a class can have access to all the classes and execute any function or alter any data any time. In such type of functions we use multiple inheritance.

here is an example of how multiple inheritance works.

```python 

class cl1: 
	def __init__(self,homie :str, roommate :str):
		self.homie = homie
		self.roommate = roommate 

	def get_homie_history(self):
		print("getting "+self.homie+" history")

class cl2:
	def get_roommate_history(self):
		print("getting "+self.roommate+" history")

class Odin(cl1,cl2):
	pass 

Odin("mukesh","ramesh").get_roommate_history()
Odin("mukesh","ramesh").get_homie_history()

```


but remember second inherited class must not have any attributes.
if both the inherited classes have the same method then the method of the class inherited first is chosen.



there was a whole lot of stuff in inheritance that is why I have coded a very good example of inheritance that covers all the concepts in one go for myself.

```python 
class phone:
    def __init__(self , price :int, color :str, camera :str):
        self.__price = price
        self.color = color
        self.camera = camer
    def show_price(self):
        return self.__price
        
class ai_camera:
    def ai_camera(self):
        return "ai camera"

  
class model1(phone):     # use of super 
    def __init__(self, price :int, color :str, camera :str, extra_features :str):
        super().__init__(price, color , camera)
        self.extra_features = extra_features
        
    def __str__(self):
        return "this phone is model 1 with price "+str(self.show_price())+" , camera "+self.camera+" ,color "+self.color+" and extra features "+self.extra_features

  

class model2(phone):         # method over riding

    def __init__(self, price :int, color :str, camera :str, discount :str):
        super().__init__(price , color , camera)
        self.discount = discount

    def show_price(self):
        price = super().show_price()
        final_price = price - self.discount
        return final_price

    def __str__(self):
        return "this phone is model 1 with price "+str(self.show_price())+" , camera "+self.camera+" ,color "+self.color+" and discount "+str(self.discount)

  
  

class model3(phone,ai_camera):               #multiple inheritance 

    def __str__(self):
        return "this is a camera with price "+str(self.show_price())+" , color "+self.color+" ,camera "+self.camera+" and camera type "+self.ai_camera()
        
model1 = model1(1000, "red", "12mp", "vedio stabalization")
model2 = model2(1000, "red", "12mp", 10)
model3 = model3(1000, "red", "12mp")

print(model1)
print(model2)
print(model3)

```

here is the class diagram 

![[Pasted image 20230820172259.png]]




## Abstraction 

In abstraction we create a law or rule or a mold class that is not used itself but is used to help create new similar classes.

for creating such a dummy or template class we need a import 

```python 
from abc import ABC , abstractmethod
``` 

abc stands for abstract in python .

here is how abstraction is done.

```python 
from abc import ABC , abstractmethod 

class template_class(ABC):

	@abstractmethod
	def show_price(self):
		pass

class car(template_class):
	def __init__(self, price):
		self.__price = price 
	def show_price(self):
		return self.price 

obj = car(10000000)
obj.show_price()


```


object of abstract class can not be created.
if the class that is abstracting another class does not have the abstract method over loaded then we will have a error.

