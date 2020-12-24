## Breakfast_plate : Based on python turtle
### Program to draw 36 pattern design.
![breakfast](https://github.com/Sid672/Breakfast_plate/blob/main/breakfast.PNG)
### Code
#### To install python turtle 
```pyhton 
pip install PythonTurtle
```
#### varibles and initialization
```python
import turtle

#screen s and turtle t
s = turtle.Screen()
t = turtle.Turtle()
turtle.bgcolor("black")

#n = 36 means 36 patterns
n = 36

#colours
col = ["red","orange","yellow","light green","blue","purple"]
j = 0
```
#### movement of turtle begin
```python
t.pencolor("purple")
t.right(270)
t.forward(25)

#main loop to draw 36 patterns
for i in range(n):

    #for 1st circle
    for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.left(360/ n)
    t.forward(25)

    #for 2nd circle
    for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.right(360/ n)

    #for change colours
    t.pencolor(col[j])
    j = j + 1
    if (j >= 6 ):
        j = 0
    t.left(10)
    t.forward(25)

turtle.done()
```
#### Every one get yummy breakfast
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/8EJ3zbKTWQ8/0.jpg)](https://www.youtube.com/watch?v=8EJ3zbKTWQ8)
