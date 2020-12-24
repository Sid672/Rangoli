## Breakfast_plate
### Program to draw 36 pattern design.
### Code
```python
import turtle

#my screen s and turtle t
s = turtle.Screen()
t = turtle.Turtle()
turtle.bgcolor("black")

#n = 36 means 36 patterns
n = 36

#colours
col = ["red","orange","yellow","light green","blue","purple"]
j = 0
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
