# Week 2: Session 2 {#week-3-session-1}

_**Looping, Data Structures, and Functions**_

#### Activity 1: Review Week 2 Session 1

* Variables
* Decision making in a program
* Logical operators
* Logical expresssions

#### **Activity 2: Demo how to create a guessing game Challenge that uses Looping**

**Identify sections of the Adventure Game framework that loop. Show**

* **how the loop is intiated**

* **what keeps it going**

* **how the loop is terminated**

#### **Activity 3: Make a Flow chart**

**Flow charts are used when designing code**

![](/assets/flow-chart-while.png)

#### **Activity 4: Write code for loops**

Code sample for while loop

```
count = 0                             # initialize
while (count < 5):                    # test to decide if we should quite
   print ('The count is:', count)     # execute instruction
   count = count + 1                  # increment counter
print ("Good bye!")                   # print good by when done with loop
```

Break out of a while loop early

```
count = 0                             # initialize
while (count < 5):                    # test to decide if we should quite
   print ('The count is:', count)    # execute instruction
   count = count + 1                 # increment counter
   if count == 3:
       break;
print ("Good bye!")                   # print good by when done with loop
```

An infinite while loop - it runs forever - it has nothing to stop it

```
var = 1
while var == 1 :  # This constructs an infinite loop
  num = raw_input("Enter a number  :")
  print "You entered: ", num

print "Good bye!"
Code sample for for loop
fruits = ["apple", "banana", "cherry"]
for x in fruits:
 print(x)
for x in range(5):
 print(x)
```

Exercise:

* Write a flow chart for a for loop

* Create a while loop

* Create a for loop

* Describe the difference between a for loop and a while loop

#### Activity 5: Python Data Structures

##### List: an ordered structure

```
animals = ['cat','dog','chicken','cow']
for animal in animals:
    print (animal, len(animal))
```

##### List: can be accessed by number and numbers start at 0

What animal get's printed with this instruction? What do "square brackets" do?

```
print ("first animal", animals[0])
```

#### Dictionary: "key:value"

Data is created by enclosing in "curly braces" and accessed by "square brackets"

```
dict =  {'name': 'Maria', 'age': 20, 'occupation': 'programmer'}
print (dict['name'], 'is a ', dict['age'], " year old ", dict["occupation"],".")
```

You can loop through all the values in a dictionary but you can't count on the order

```
for key, value in dict.items():
    print (key, value)
```

You can create a list of dictionary items,  Is it OK to use single quotes or double quotes when creating dictionaries?

Why do I need 2 "for" loops to do the following? What is the output?

```
list = [{'one':1}, {"two":2}, {'three':3} ]
for item in list:
    for key, value in item.items():
        print (key, value)
```

#### **Activity 6: Functions**

Functions help to organize code and prevent duplicating code through the program. A function is a named chunk of code that can be called from another section of the program. It can define parameters which are variables that will be passed to it when called. Functions can also return values.

We'll do exercises in which we write and call functions withparametersandreturnvalues. For example we can write a function that takes two numbers, adds them together and returns the sum. We'll also incorporate functions into the code we write for the Challenge.

**Exercise:**

* Create and call a function that has no parameters and returns nothing
* Create and call a function that has parameters and returns a value
* Create a function that:
  * accepts a number number as a parameter
  * uses the parameter to initialize a loop
  * return the value of the number at the end of the loop

**Activity 6: Write a Challenge for the game**

For example

```
def guess_function(num,howMany):
  for i in range(0, howMany):
    question = "Give me a number between 1 and " + str(howMany)
    guess = input(question)
    try:
        guess = int(guess)
        if guess == num:
            return True
        elif guess < num:
            print("Try higher")
        elif guess > num:
            print("Try lower")
    except:
        print("That was not a number. Try again")
  return False

if guess_function(3,5):
  print ("yay")
else:
  print ("nay")
```

#### **Activity 7: Write a Challenge for the Game that uses Looping and Functions**



