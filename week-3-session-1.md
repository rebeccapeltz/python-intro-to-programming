# Week 3: Session 1

_**File I/O and the Operating System**_

The computer's file system is made up of files and directories.  Directories may contain files.  Files contain data.

#### Activity 1: Review Week 2

* Decision making
* Logical Operators and Expressions
* Looping

#### Activity 2: Demostrate where file I/O is used in the Game.

#### **Activity 3: What is I/O?  Input/Output**

Review Console I/O

```
str = input("Input your favorite color? ")
print ("Outputting your favorite color: ",str)
```

**First, Create a file by Writing to It**

What does "\#write" mean?

```
#write
myfile = open("myfile","w")
myfile.write("hello")
myfile.close()
print (myfile.name, "is open?", myfile.closed)
```

**Next, Read the file and write its contents to the console**

```
#read
myfile = open("myfile","r")
str = myfile.read()
print ("contents of ",myfile.name,": ",str)
myfile.close()
```

##### Exercise

Create a text file in the IDE \(manually without code\).

Write a program that read the data from the file and writes the output to the console.

Write a program that asks the user a question and then writes the answer to a file.

Write a program that reads the file and prints the output to the console.

What happens if you run the read file program before the write  file program?

#### Activity 4: What is "os"? Operating System

##### Test that a file exists

```
print("this file exists?",os.path.isfile("file-exists.py") )
```

**Renaming a file**

**What is the import command doing?  What is "os"?**

```
import os
os.rename( "myfile.txt", "test.txt" )
```

**Removing a file**

```
import os
os.remove("test.txt")
```

##### Working with Directories and Calling Programs from Code

Make a directory and then go to it to make a file.  What does "../" mean?

```
import os

os.mkdir("test")
os.chdir("test")
os.system("python ../file-write.py")
```

#### Activity 5: Create a challenge that uses a file

Create a file with a question.

Read the file to get a question that you ask for the challenge.

#### 



