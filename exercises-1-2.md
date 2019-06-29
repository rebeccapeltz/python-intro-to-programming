# Exercises 1-2
This exercise can be found in Chapter 2 in the course text. You will have 4 "programs" to write. These all take user input, perform some operation on that input and return some output. All numbers should be rounded to two (2) decimal points. NOTE: Make sure you're forcing your inputs that take integers to integer type variables.

Input/Output or "I/O" is a critical part of programming. In Concepts in Computing you should have learned about the notion of encapsulation and black-boxing. As a reminder, when we develop programs, our goal is to create a program that takes in a certain kind of input and if that input fits the parameters of the program will return a predictable kind of output. The process that converts input to output is often hidden (ie. blackboxed), which can be problematic (what if that process is logging your email address, for instance), but understanding the I/O model will help you write better programs.

## Question 1: 
Write a program that uses the input() function to prompt a user for their name, and then welcomes them. On this activity, I've given you a head start

      Enter your name: Dylan

      Hello Dylan



## Question 2: 
Write a program that prompts a user for hours and rate per hour to compute gross pay. The program should print out gross pay. It should also print out the percentage of the Federal Minimum Wage ($7.25) and of the Seattle Minimum Wage ($15) that gross pay would be. Here's the calculation:

      percent_fed = gross_pay/(hours*7.25) * 100.

      percent_sea = gross_pay/(hours*15) * 100.




## Question 3:
Next write a program that converts Fahrenheit to Celsius. The user input will be a temperature in degrees Fahrenheit and the output will be that temperature in Celsius. 

      C = (F - 32) * (5/9)


## Question 4: 
Finally, you'll often split bills simply by how many people are there, but what if you're going out with your rich friends? What if you are your rich friends and people who make less are going out with you? Let's make a calculator that's more equitable and splits a bill based on how much each of you make. The program needs to take as input three incomes and the bill amount. It should print out the share of the bill that each person should pay. Hint: Try to figure out what percentage of your total income each of you makes and apply that to the bill.