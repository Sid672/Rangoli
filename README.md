## Breakfast_plate : Based on python turtle
[Link to the demo and code.](https://repl.it/@Siddharthsing13/testpy#main.py)
### Program to draw 36 pattern design.
![358eazWwzOU6c](https://media.giphy.com/media/358eazWwzOU6c/giphy.gif)
# YOUR PLATE
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

### Let's start
Create a new Python project on repl.it by visiting https://repl.it/languages/python3

![KRiymXy9LEKXwQMUGv](https://media.giphy.com/media/KRiymXy9LEKXwQMUGv/giphy.gif)


## 5 Steps to draw breakfast plate:
### 1) Install python turtle 
```pyhton 
pip install PythonTurtle
```
### 2) Import python turtle and set screen and turtle name
```python
import turtle
s = turtle.Screen()
t = turtle.Turtle()
```
### 3) Set color of background and pen
```python
#color of background
turtle.bgcolor("black")
#color of pen
col = ["red","orange","yellow","light green","blue","purple"]
j = 0
t.pencolor("purple")
```
### 4) Movement of turtle begin
```python
#n = 36 means repeat same pattern 36 times.
n = 36
t.right(270)
t.forward(25)
```
#### 4.1)Main loop to draw 36 pattern
```python
for i in range(n):
```
#### 4.2)Loop to draw 1st small circle
```python
//nested loop
 for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.left(360/ n)
    t.forward(25)
```
#### 4.3)Loop to draw 2nd small circle
```python
    for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.right(360/ n)
```
### 5) Change color of pen
```python
    t.pencolor(col[j])
    j = j + 1
    if (j >= 6 ):
        j = 0
    t.left(10)
    t.forward(25)

turtle.done()
```
# Your code looks like:
After completing all steps code seems like this
```python
#2)Import python turtle and set screen and turtle name

import turtle
s = turtle.Screen()
t = turtle.Turtle()

#3) Set color of background and pen

#color of background
turtle.bgcolor("black")
#color of pen
col = ["red","orange","yellow","light green","blue","purple"]
j = 0
t.pencolor("purple")


#4) Movement of turtle begin

#n = 36 means repeat same pattern 36 times.
n = 36
t.right(270)
t.forward(25)

#Main loop to draw 36 pattern
for i in range(n):

# Loop to draw 1st small circle
  for i in range(int((3 * n) / 4)):
      t.forward(0.8)
      t.left(360/ n)
  t.forward(25)

# Loop to draw 2nd small circle
  for i in range(int((3 * n) / 4)):
      t.forward(0.8)
      t.right(360/ n)


# 5) Change color of pen

  t.pencolor(col[j])
  j = j + 1
  if (j >= 6 ):
      j = 0
  t.left(10)
  t.forward(25)

turtle.done()
```
# Run code:
Click the green "Run" button on the top of the repl.it windows. A screen will be shown on the right side displaying the turtle graphics that you coded. If you face any errors, try commenting out each portion of the code and making only a certain section work. This generally helps to figure out the error.
Run your code and watch turtle how it moves...
![breakfast2](https://github.com/Sid672/Breakfast_plate/blob/main/breakfast2.PNG)

Your output will be:
![breakfast1](https://github.com/Sid672/Breakfast_plate/blob/main/breakfast1.PNG)


# Enjoy breakfast
![nJ2PObJA3EVgc](https://media.giphy.com/media/nJ2PObJA3EVgc/giphy.gif)

