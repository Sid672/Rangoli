## Breakfast_plate : Based on python turtle
### Program to draw 36 pattern design.
![breakfast](https://github.com/Sid672/Breakfast_plate/blob/main/breakfast.PNG)
### Functions used:
| Method          | Parameter                              | Description                                                                      |
| --------------- | -------------------------------------- | ---------------------------------------------------------------------------------| 
| turtle()        | None                                   | Creates and returns a new turtle object                                          | 
| right()         | value of angle is degree               | Turns the turtle clockwise                                                       | 
| left()          | value of angle is degree               | Turns the turtle counter clockwise                                               |
| forward()       | distance – a number (integer or float) | Moves the turtle forward by the specified amount                                 | 
| pencolor()      | Color name                             | Changes the color of the turtle’s pen                                            | 
| bgcolor()       | Color name                             | Changes the color of the background                                              |
| done()          | None                                   | This function is used to starts event loop – calling Tkinter’s main loop function|                                 

### 5 Steps to draw breakfast plate:
#### 1) Install python turtle 
```pyhton 
pip install PythonTurtle
```
#### 2) Import pyhton turtle and set screen and turtle name
```
import turtle
s = turtle.Screen()
t = turtle.Turtle()
```
#### 3) Set color of background and pen
```
#color of background
turtle.bgcolor("black")
#color of pen
col = ["red","orange","yellow","light green","blue","purple"]
j = 0
t.pencolor("purple")
```
#### 4) Movement of turtle begin
```
#n = 36 means repeat same pattern 36 times.
n = 36
t.right(270)
t.forward(25)
```
##### Main loop to draw 36 pattern
```
for i in range(n):
   \\body
```
##### Loop to draw 1st small circle
```
 for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.left(360/ n)
    t.forward(25)
```
##### Loop to draw 2nd small circle
```
    for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.right(360/ n)
```
#### 5) Change color of pen
```
    t.pencolor(col[j])
    j = j + 1
    if (j >= 6 ):
        j = 0
    t.left(10)
    t.forward(25)

turtle.done()
```

#### Every one get yummy breakfast

