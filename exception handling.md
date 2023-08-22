we as programmers can control errors but we cannot control exceptions in a code.

for example we can write a code that can divide two numbers and gives the numerator.

```python 

a = int(input("enter the first number "))
b = int(intput("enter the secong number "))

c = a/b 

print(c)
```

in this case there are two kinds of exceptions that can occur and we can also manage them easily.

exception 1:
when user tries to divide the number by zero (zerodivisionerror)

![[Pasted image 20230821162211.png]]

exception  2: 
when user tries to enter an alphabet or any character.

![[Pasted image 20230821162305.png]]

now here is the solution for managing these kind of errors from the user side. Remember you are a engineer but the user can be dumb. SO for being on the safe side we make the code such that it does not abruptly end the program , instead it executes another set of code for a specific or a group of exceptions.

```python 
try:
    a = int(input("enter the first number "))
    b = int(input("enter the secong number "))
    c = a/b
    print(c)

  

except ZeroDivisionError as e:
    print(e)
    print("you cannot divide a number by 0")

  

except ValueError as e:
    print(e)
    print("you must enter a number")
```

`as e ` is just assigning the type of error to e and then using it for a good cause 


now this code with not let the program end abruptly .

we can also add else block to only give the results when there is no errors, as it can save system resources and gives a chance  to correct the incorrect.

here is how it is done.

```python 
try:

    a = int(input("enter the first number "))

    b = int(input("enter the secong number "))

    c = a/b

  

except ZeroDivisionError as e:

    print(e)

    print("you cannot divide a number by 0")

  

except ValueError as e:

    print(e)

    print("you must enter a number")

  

else:

    print(c)
```

#### use of finally 

there are some case when we need to run some code that is hell important can cannot be skipped due to a exception in between. 

example of some can be a ATM program, even if the transaction fails the program calls itself to maintain a loop. Text editors also have it so that they save the file in case of any errors, to safe the loss of data. 

here is how it is used:

```python 
try:

    a = int(input("enter the first number "))

    b = int(input("enter the secong number "))

    c = a/b

  

except ZeroDivisionError as e:

    print(e)

    print("you cannot divide a number by 0")

  

except ValueError as e:

    print(e)

    print("you must enter a number")

  

else:

    print(c)

  

finally:

    print("finally always runs ")
```

output 
```
enter the first number 2 
enter the secong number 0
division by zero
you cannot divide a number by 0
finally always runs 

```

### custom exceptions 

yes we can also create our own exceptions to make the process easy of programmers and make the algos much simpler.




### Object oriented aspect of exception handling

It is prety easy to get started in object oriented aspect of exception handling 

you just need to inherit `Exception` class in a custom class and  then it gest called when exception is raised.

```python
class I_am_an_exception(Exception):

    print("I am an exception")

try:

    raise I_am_an_exception

except Exception as e:

    pass
```

output:
'I am an exception'

and yes that's it.

the story ends :)