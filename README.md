---
name: 'Rangoli'
description: 'Rangoli with python turtle!'
author: 'Sid672'
image: 'https://github.com/Sid672/Rangoli/blob/main/rangoli.PNG?raw=true'
---
# Rangoli

![](https://github.com/Sid672/Rangoli/blob/main/rangoli.PNG?raw=true)

[Demo Link](https://repl.it/@Siddharthsing13/rangoli#main.py)

# Let's start
Let me introduce " repl. it " to you, its an online platform that runs code in all languages. It's a friendly platform to test and show code.  
Now, create a new python project on [repl.it](https://repl.it/languages/python3). 

- You can also follow steps in demo video to create repl.

![](https://media.giphy.com/media/3y8Rl5IC2gKjhfdGLQ/giphy.gif)

# Functions 
- Before any project everyone need some knowledge. Don't worry you don't need to remember all keywords. Only try to understand use of functions.
- These functions are used in the program. So atleast once, read it.


| Method          | Parameter                              | Description                                                                      |
| --------------- | -------------------------------------- | ---------------------------------------------------------------------------------| 
| turtle()        | None                                   | Creates and returns a new turtle object                                          | 
| right()         | value of angle is degree               | Turns the turtle clockwise                                                       | 
| left()          | value of angle is degree               | Turns the turtle counter clockwise                                               |
| forward()       | distance – a number (integer or float) | Moves the turtle forward by the specified amount                                 | 
| pencolor()      | Color name                             | Changes the color of the turtle’s pen                                            |
| fillcolor()	   | Color name	                          | Changes the color of the turtle will use to fill a polygon                       |
| goto()	         | x, y	                                | Move the turtle to position x,y                                                  |
| up()	         | None	                                | Picks up the turtle’s Pen                                                        |
| down()	         | None	                                | Puts down the turtle’s Pen                                                       |
| bgpic()         | image name                             | Changes the background                                                           |
| stamp()	      | None	                                | Leaves an impression of a turtle shape at the current location                   |
| shape()	      | shapename	                             | Should be ‘arrow’, ‘classic’, ‘turtle’ or ‘circle’                               |
| setup()         | width, height                          | Sets screen size                                                                 |
| speed()         | value in integer                       | Increases turtle speed. fastest: 0, fast: 10, normal: 6, slow: 3, slowest: 1     |  
| done()          | None                                   | This function is used to starts event loop – calling Tkinter’s main loop function| 



#  Steps:
We can divide program in four parts.  
- Background
- Outer pattern
- Inner pattern
- Combination: outer + inner patterns

![](https://github.com/Sid672/Rangoli/blob/main/steps.png)

# Background

### Python turtle library
- Python turtle library is a popular way for introducing programming to kids. We can make shapes, patterns, can learn about functions, loops, varibles and lot more in programming. It's like baby building blocks for coders.

We know that before drawing anything we need paper, pen and colours. In python turtle, screen is your paper, turtle is pen and we can change colours of pen.
- To import python turtle library write line `import turtle`.
- To setup a screen(paper) we need a varible `s = turtle.Screen()`. By this varible we can set background colours, add images on screen and change the size of screen. In the same way a varible for pen `t = turtle.Turtle()` is use to draw.
- `turtle.done()` is used to pause the screen after excution of code. Otherwise you can't see the pattern after execution.
- Start with this simple code and run it then you will get programming environment of python turtle.
```python
import turtle
s = turtle.Screen()
t = turtle.Turtle()
turtle.done()
```
- The programming environment for python turtle looks like this:
![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_1.PNG?raw=true)

- Now its time to choose background image you can download some images or use image you have. You should upload that image on your repl first. 
- Link of image used in project [link](https://github.com/Sid672/Rangoli/blob/main/back.jpg) 
- To upload image click on last option of `Files` which is above of `main.py` then choose Upload file.
![](https://github.com/Sid672/Rangoli/blob/main/back1.PNG)

- After uploading image then setup screen size `s.setup(width, height)`. 
- To set background  `s.bgpic("imagename.png/jpg")` is used.
```Python
s.setup(626, 313)
s.bgpic("back.jpg")
```
Add these two lines before `turtle.done()` then run you will get your background.
![](https://github.com/Sid672/Rangoli/blob/main/back2.PNG)

![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_2.PNG?raw=true)

# Outer Pattern

## Let's draw
- `Tip: Before drawing anything on python turtle you should draw it on paper.`

![](https://media.giphy.com/media/hmRzYbArCq1i6rFfmo/giphy.gif)

These are my rough diagram of Rangoli. Don't worry if you are not good in drawing, it's ok. The rough figure is basically used for calculations of length (in pixels) and angle (in degrees).

![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_9.PNG?raw=true)
![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_10.PNG?raw=true)

- We can design outer pattern in lot of varitions. In this project we are using only one variation you can try other variations also.

- Other variations looks like.
![](https://github.com/Sid672/Rangoli/blob/main/v.png?raw=true)

- Now we should focus back on project design then with simple change in code we can acchive other variations also. 
- Since all patterns are colour full so we need colours.
- Original colour of pen is black. We can change colour of pen by using a list.
- List is like a container so we can store our colours in list `col = ["red","orange","yellow","green","blue","purple"]`. We also need a varible to access the colours `j = 0`. 
```
Example- col[j] = red, when j = 0
col[j] = orange, when j = 1
```
- By changing the value of j, we change colour of pen.
- We should initialize the colour of pen for this `t.pencolor("purple")` is used.
```Python
#Colours :
col = ["red","orange","yellow","green","blue","purple"]
j = 0
t.pencolor("purple")
```
- We can't draw outer pattern from cetre because if we do that then outer and inner pattern will intersect.
- To manage it use `t.up()`. It move pen up from paper.Otherwise if we change coordinates from (0, 0)(initial coordinates) to (x, y)(new position)
pen will make a line between two points.
- Then set coordinates `t.goto(x, y)` and pen down `t.down()`.
- To get correct coordinate we should test code 2 to 3 times after both pattern are completed.
```Python
t.up()
t.goto(80, -100)
t.down()
```
We need to understand some terms before drawing.
- Pixel is the smallest measurable unit on screen.
- Nested loop
   - loop inside loop.
```example - 
Outer loop:
   Inner loop:
     #body
```
- You have seen that the same pattern is repeated. If you count, you will find that pattern is repeated 36 times. So we need a varible `n = 36`.
- According to rough diagram we should turn turtle upward `t.right(270)`then move 25 pixels `t.forward(25)`.
```python
n = 36                                          
t.right(270)
t.forward(25)
```
![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_7.PNG?raw=true)

- Next, we use some loops, main loop will repeat 36 times because n = 36.
- We fill colour in turtle(pen) by `t.fillcolor(col[j])` and change its shape `arrow --> circle`   after that we print it on paper `t.stamp()`.
- Nested loop repeat `int((3 * n) / 4) = 21 times`.
- Then `t.forward(0.8)`means pen will move 0.8 pixel , `t.left(360/ n)` turn left 10 degrees because `360/ n = 10 degrees`.
- To join circle and arrow pen move forward 25 pixels and change its shape again `circle --> arrow` then we print it again.
- In similar way we repeat next loop in rigth direction to acchive circular path.
- To change colour of pen use `t.pencolor(colour name)`.
- But remember our colour container `col = ["red","orange","yellow","green","blue","purple"]` contains only 6 colours numbered from (col[j = 0] = red,.... col[j = 5] = purple).
- So j can't be greater than and equal to 6. 
- To maintain j we use condition ` if (j >= 6 ): j = 0 `.
```Python
#main loop
for i in range(n):
   t.fillcolor(col[j])
   t.shape('circle')
   t.stamp()
   
   #nested loop
   for i in range(int((3 * n) / 4)):
       t.forward(0.8)
       t.left(360/ n)
   
   #line to join partterns 
   t.forward(25)
   t.shape('arrow')
   t.stamp()
   
   for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.right(360/ n)
        
   #line to join patterns     
   t.left(10)
   t.forward(25)
   
   #colour change of pen
   t.pencolor(col[j])
   j = j + 1
   if (j >= 6 ):
      j = 0

```
![Inamge]()

# Inner pattern
- It is better draw inner pattern sepratly because we can try different combinations with outer pattern.
- First we set coordinates of coordinates because of outer pattern our cooridnates are not (0, 0).
- So we should correct it. For this we again use `t.up()`, `t.goto(0, 0)` and `t.down()`.
```Python 
t.up()
t.goto(0, 0)
t.down()
```
- Now we change the shape of pen `t.shape('arrow')`.
- Its time to decide shape of inner pattern we can use triangle, square, rectangl,..... any (n-sided) polygon.
- In this project we are using 10 sided polygon. 
- We use a loop to draw a polygon `for i in range(n):` then repeat same polygon in circular path `for i in range(m):` is used.
- To draw polygon we move `t.forward(24)`, then turn `t.right(360.0/ n)`.
- Again we need some colours so we set `t.pencolor("blue")`.
- To make pattern more beautiful we fill colour in pen and print(`t.stamp()`) it after completing each line.
- We should turn pen, then it will draw same polygon at different angle. In this way circular path is acchived.

```Python
#for 10 sided polygon
n = 10

#to move in circular path
m = 10

for i in range(m):
   for i in range (n):
       t.forward(24)
       t.right(360.0/(n))
       t.pencolor("blue")
       t.fillcolor("blue")
       t.stamp()
   t.right(360.0/n)
```
- In same way, we will draw two more design with `t.pencolor("green")` and `t.pencolor("red")`.
```Python
for i in range (m):

  for i in range(n):
       t.pencolor("green")
       t.fillcolor("green")
       t.forward(26)
       t.left(360.0/(n))
       t.stamp()
  
  t.left(360.0/n)


for i in range(m):

   for i in range(n):
       t.pencolor("red")
       t.fillcolor("red")
       t.forward(28)
       t.right(360.0/(n))
       t.stamp()
   
   t.right(360.0/n)
```
- Now we combine all design. Your final design looks like
![](https://github.com/Sid672/Rangoli/blob/main/c1.png?raw=true)

- In inner design we need an outline.
- To outline design we use same polygon loop but this time without printing pen shape.
- To project make more intreseting we use different shape of pen `t.shape('turtle')`.
```Python
t.shape('turtle')
for i in range(m): 

  for i in range(n):
    t.pencolor("black")
    t.forward(30)
    t.right(360.0/(n))
    
  t.right(360.0/n)
```

# Your code looks like this:
After completing all steps, the code looks like this.
```python

import turtle
s = turtle.Screen()
t = turtle.Turtle()
#color of background
turtle.bgcolor("black")
#color of pen
col = ["red","orange","yellow","light green","blue","purple"]
j = 0
t.pencolor("purple")
n = 36
t.right(270)
t.forward(25)
for i in range(n):
   for i in range(int((3 * n) / 4)):
       t.forward(0.8)
       t.left(360/ n)
   t.forward(25)
   for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.right(360/ n)
   t.left(10)
   t.forward(25)
   t.pencolor(col[j])
   j = j + 1
   if (j >= 6 ):
      j = 0

turtle.done()

```
# Run code:
Click the green "Run" button on the top of the ``repl. it`` windows. A screen will be shown on the right side, displaying the turtle graphics you coded. If you face any errors, try commenting out each portion of the code and making only a certain section work. It generally helps to figure out the error.

Run your code and watch the turtle how it moves

![breakfast2](https://github.com/Sid672/Breakfast_plate/blob/main/breakfast2.PNG)

Your output will be:
![breakfast1](https://github.com/Sid672/Breakfast_plate/blob/main/breakfast1.PNG)


# Enjoy breakfast
## Great work, you made it!
![nJ2PObJA3EVgc](https://media.giphy.com/media/nJ2PObJA3EVgc/giphy.gif)

# Links of all demos
### Complete Breakfast plate
[Code Link](https://repl.it/@Siddharthsing13/breakfast#main.py)
### Simple pattern
[Code Link](https://repl.it/@Siddharthsing13/demobreakfast2#main.py)
### Stair pattern
[Code Link](https://repl.it/@Siddharthsing13/demobreakfast3#main.py)

# Cool examples:
These are some enjoyable projects, where the turtle screen act's like a canvas and can be used to draw diagrams and patterns like these pictures.

![1536865435321_bd598138637586247b2433a96371534d](https://storage.googleapis.com/replit/images/1536865435321_bd598138637586247b2433a96371534d.pn)
![1536865448102_a542f76811f1df3d35a97ffd613c3e39](https://storage.googleapis.com/replit/images/1536865448102_a542f76811f1df3d35a97ffd613c3e39.pn)

To draw both diagrams, use the code link.

[Code Link](https://repl.it/@Siddharthsing13/Coolproject1#main.py)

# Happy Hacking:
Now it's your turn to make your lunch and dinner plate. You can share your design on [Link](https://hackclub.slack.com/archives/C01504DCLVD). I would love to see your creation. Keep enjoying, keep hacking!
