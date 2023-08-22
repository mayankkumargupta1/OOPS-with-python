Imagine a situation when you need to handle a whole lot of similar objects or objects of the same category.

writing code to use each object would be a haptic task 

a better approach would be to store all the objects into a single list and then use a loop to do the same task for all.

here is a situation, shopkeeper wants to see the prices of all the soaps he has 

```python 
class soap:
    def __init__(self,price,shape):
        self.shape = shape
        self.__price = price

    def __str__(self):
        print("this is a soap object with id ",self.id)
        
	def get_price(self):
	    return self.__price 

soap1 = soap(100,"oval")
soap2 = soap(300,"round")
soap3 = soap(10,"triangle")
soap4 = soap(30,"rectangle")
soap5 = soap(50,"oval")
soap6 = soap(120,"oval")

lst_of_soaps = [soap1,soap2,soap3,soap4,soap5,soap6]

for soap in lst_of_soaps:
	print("price",soap.get_price(),"shape",soap.shape)
	
```

this can also be done with dictionary
