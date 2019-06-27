#### List of Turtle Commands

| Command | What is does | Example |
| :--- | :--- | :--- |
| forward\(distance\) | If distance is positive turtle will move forward and if negative turtle will move backward | forward\(10\), forward\(-10\) |
| backward\(distance\) | If distance is positive turtle will move backward and if negative turtle will ove forward | backward\(10\), backward\(-10\) |
| right\(angle\) | Current direction is changed in the direction of the angle in a clockwise direction | right\(90\), right\(10\) |
| left\(angle\) | Current direction is changed in the direction of the angle in a counter clockwise direction | left\(90\), left\(10\) |
| goto\(x, y\) | Move the turtle to the absolute position of x, y in the canvas grid | goto\(0,0\), goto\(-10, -10\) |
| setx\(x\) | Move to the x position and don't change y | setx\(0\), setx\(-300\) |
| sety\(y\) | Move to the y position and don't change x | sety\(0\), sety\(-300\) |
| setheading\(angle\) | Sets turtle in a direction given by angle | setheading\(90\) |
| home\(\) | Move the turtle to the home position which is \(0,0\) | home\(\) |
| pendown\(\) |  |  |
| penup\(\) |  |  |
| pensize\(size\) |  |  |
| pencolor\(\) |  | pencolor\(red\) |
| fillcolor\(color\) |  | fillcolor\(red\), fillcolor\(red, green, blue\) |
| begin\_fill\(\) |  |  |
| end\_fill\(\) |  |  |
| stamp\(\) | Prints a stamp |  |
| listen\(\) | Program listens for interactive commands like key up, key down, key left, key right | see interactive code below |
| onkey\(\) | Calls a function based on keystroke detected in listen | onkey\(up, 'Up'\) |

#### Interactive Listening 

```
from turtle import *

def up():
    setheading(90)
    forward(100)

def down():
    setheading(270)
    forward(100)

def left():
    setheading(180)
    forward(100)

def right():
    setheading(0)
    forward(100)

listen()

onkey(up, 'Up')
onkey(down, 'Down')
onkey(left, 'Left')
onkey(right, 'Right')

onkey(up, 'w')
onkey(down, 's')
onkey(left, 'a')
onkey(right, 'd')
```



