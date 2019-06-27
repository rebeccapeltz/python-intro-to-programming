# Week 4: Session 1

_**Classes, Objects, Modules, Packages and Libraries**_

#### Activity 1: Review Week 3

Input/Output

File I/O

JSON

Internet API's

#### Activity 2: Demonstrate where Classes and Objects are used in the Game

#### Activity 3: Intro to Classes and Objects/Modules and libraries

As programs grow, it becomes important to organize and **encapsulate** both data and functionality.  We are always looking for ways to share code in way that allows us to just write the code once and not rely on copy/paste to share it.

**Objects** are nouns and can be described by their parts, or characteristics \(adjectives\) and what they can do \(verbs\)

**Classes** allow us to define code in the way we would define an object in real life.

The class code is a template for the object, and when we want to use the object we get an **instance** of a specific object.

**Modules **are code chunks such as classes, stand alone functions and constants that are stored in a file and can be imported into another file.  Look at the code for the python os module:[ https://github.com/python/cpython/blob/master/Lib/os.py](https://github.com/python/cpython/blob/master/Lib/os.py)

**Packages** are a collection of Modules.  It is a directory with a collection of files and an \_\_init\_\_.py file which distinguishes it from just a directory with a bunch of python scripts.  We think of the directory as a **namespace** which means I can have a file called **update.py** in a directory that is a package named "Student" and Student.update would be different than a update.py not in the package.  Namespacing allows us to reuse names for files.  

**Libraries **are containers for packages. Look at the code for python's numPi library: [https://github.com/numpy/numpy/tree/master/numpy](https://github.com/numpy/numpy/tree/master/numpy)

**Exercise**:

Let's define a car class

characteristics \(nouns and adjectives\): make, model, color, year, max speed

what they can doe \(verbs\): start, stop, brake, move forward, move in reverse, park

#### Activity 4: Code a class

Code a car object using Python language elements shown below

> **class**     This defines the name of the object template
>
> **self**        This is the variable that the object uses to refer to itself in code
>
> **def**        This is how you define a data or method
>
> **\_\_init\_\_**  This is code that runs when we want to create a new instance of the class which is an object
>
> **return**    Some methods can return data as we learned with functions

**Exercise**:

Get the car object code running and add a function to accellerate \(increase speed\). Use the code below to start.

```
# define Car template
class Car:
    def __init__(self, year, make, model, color, max_speed):
        self.__year = year
        self.__make = make
        self.__model = year
        self.__color = color
        self.__max_speed = max_speed
        self.__current_speed = 0
        print("You now have a car with these features:")
        print("year: ", self.__year)
        print("make: ", self.__make)
        print("model: ", self.__model)
        print("color: ", self.__color)
        print("max_speed: ", self.__max_speed)
        print("current speed: ", self.__current_speed)

    def start(self):
        print('Car starting')

    def stop(self):
        print('Car stopping')

    def move_forward(self):
        print('Moving forward')

    def move_reverse(self):
        print('Moving in reverse')

    def set_speed(self, speed):
        self.__current_speed = speed
        print('Moving at this speed now:', self.__current_speed)

    def brake(self):
        if self.__current_speed > 0:
            self.__current_speed = self.__current_speed - 1

    def park(self):
        print('Parking')

    def get_speed(self):
        return self.__current_speed
```

#### Activity 5: Code for instantiating an Object from a Class

First we write function \(main\) that instantiates the class to create a specific object.  Then we call the function \(main\(\)\) to execute it.

**Exercise**

Code a main function that gets an instance of the car class.  Only the start method is called in the code in main.

```
# function to instantiate the class
def main():

    year = input('Enter the car year: ')
    color = input('Enter the car color: ')
    make = input('Enter the car make: ')
    model = input('Enter the car model: ')
    max_speed = input('Enter the car\'s max speed:')

# instantiate a car
    mycar = Car(year, make, model, color, max_speed)

 # call methods on car
    mycar.start()


# call main
main()
```

#### Activity 6: Modules

Modules help us to organize code into a separate files. Using the import command we can access module code from another file.

The import command names the file \(without the .py extension\) that contains the code you want to import.  You can reference functions in that file by using the dot\(.\).

**Exercise**

Create a file \(name\_prompt.py\) that contains a function that asks you your name.

Create a file \(use\_name\_prompt.py\) that import the first file and executes the function in it.

Here's an example of two files \(name\__prompt.py and use\_name\_prompt.py\) that are working together using the import command._

```
# age_prompt.py
def ask_age():
  age = input("Enter your age:")
  return age
```

```
# use_age_prompt.py
import age_prompt

age = age_prompt.ask_age()
print("Hello ",age," year old!")
```

#### Activity 7: Install and Import Libraries

Libraries are made available by package managers like pip.  We'll look at libraries we've used and try out some new libraries.

