---
name: 'Rangoli'
description: 'Rangoli with python turtle!'
author: 'Sid672'
image: 'https://github.com/Sid672/Rangoli/blob/main/rangoli.PNG?raw=true'
---
# Rangoli
Hey!,
Have you heard of Rangoli?

If yes, great!. If no, don't worry I am here for you. 

Rangoli is an art form, originating in the Indian subcontinent, in which patterns are created on the floor or the ground using materials such as colored rice, colored sand, quartz powder, flower petals, and colored rocks. And today we are going to create this beautiful pattern in just a few clicks.

![](https://github.com/Sid672/Rangoli/blob/main/rangoli.PNG?raw=true)

[Demo Link](https://repl.it/@Siddharthsing13/rangoli#main.py)

# Let's start
Let me introduce " repl. it " to you, its an online platform that runs code in all languages. It's a friendly platform to test and show code.  
Now, create a new python project on [repl.it](https://repl.it/languages/python3). 

- You can also follow steps in demo video to create repl.

![](https://media.giphy.com/media/3y8Rl5IC2gKjhfdGLQ/giphy.gif)

# Functions 
- Before any project, everyone needs some knowledge. Don't worry, you don't need to remember all keywords. Only try to understand the use of         functions.
- The functions that we use in the program are given below. So at least read it once.


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
We can divide the program into four parts.  
- Background
- Outer pattern
- Inner pattern
- Combination: outer + inner patterns

![](https://github.com/Sid672/Rangoli/blob/main/steps.png)

# Background

### Python turtle library
- Python turtle library is a popular way for introducing programming to kids. We can make shapes, patterns can learn about functions, loops, variables, and a lot more in programming. It's like baby building blocks for coders.

We know that before drawing anything we need paper, a pen, and colors. In the python turtle, the screen is your paper, the turtle is a pen and we can change the colors of the pen.
- To import python turtle library write line `import turtle`.
- To set up a screen(paper) we need a variable `s = turtle.Screen()`. By this variable, we can set background colors, add images on the screen and change the size of the screen. In the same way a variable for pen `t = turtle.Turtle()` is used to draw.
- `turtle. done()` is used to pause the screen after the execution of code. Otherwise, you can't see the pattern after execution.
- Start with this simple code and run it, then you will get the programming environment of python turtle.
```python
import turtle
s = turtle.Screen()
t = turtle.Turtle()
turtle.done()
```
- The programming environment for python turtle looks like this:
![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_1.PNG?raw=true)

- Now it's time to choose a background image you can download some images or use an image, you have. You should upload that image on your repl first. 
- Link of the image used in the project : [link](https://github.com/Sid672/Rangoli/blob/main/back.jpg) 
- To upload an image click on the last option of `Files` which is above `main.py` then choose Upload file.
![](https://github.com/Sid672/Rangoli/blob/main/back1.PNG)

- After uploading image then setup screen size `s.setup(width, height)`. 
- To set background  `s.bgpic("imagename.png/jpg")` is used.
- Since our pattern large so we need to move turtle fastest as possible.
- To do this we use `t.speed(0)`, 0 is used for fastest.
```Python
s.setup(626, 313)
s.bgpic("back.jpg")
t.speed(0)
```
Add these lines before `turtle. done()` then run it, we will get our background.
![](https://github.com/Sid672/Rangoli/blob/main/back2.PNG)

![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_2.PNG?raw=true)

# Outer Pattern

## Let's draw
- `Tip: Before drawing anything on python turtle, you should draw it on paper.`

![](https://media.giphy.com/media/hmRzYbArCq1i6rFfmo/giphy.gif)

These are my rough diagram of Rangoli. Don't worry if you are not good at drawing it's ok. The rough figure is basically used for calculations of length (in pixels) and angle (in degrees).

![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_9.PNG?raw=true)
![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_10.PNG?raw=true)

- We can design outer patterns in a lot of variations. In this project we are using only one variation you can try other variations also.

- Other variations look like.
![](https://github.com/Sid672/Rangoli/blob/main/v.png?raw=true)

- Now we should focus back on project design then with a simple code change we can achieve other variations also. 
- Since all patterns are colorful so we need some colors.
- Original color of the pen is black. We can change the color of a pen by using a list.
- List is like a container so we can store our colors in it. `col = ["red","orange","yellow","green","blue","purple"]`. We also need a varible to access the colors `j = 0`. 
```
Example- col[j] = red, when j = 0
col[j] = orange, when j = 1
```
- By changing the value of j, we can change the color of the pen.
- We should initialize the color of the pen using `t.pencolor("purple")`.

```Python
#Colours :
col = ["red","orange","yellow","green","blue","purple"]
j = 0
t.pencolor("purple")
```
- It's not a good idea to draw an outer pattern from the center because if we do that then the outer and inner pattern will intersect.
- To manage it use `t.up()`. It moves the pen up from the paper. Otherwise, if we change coordinates from (0, 0)(initial coordinates) to (x, y)(new position)
the pen will trace the path between two points.
- Then set coordinates using `t.goto(x, y)` and pen down  by `t.down()`.
- To get the coordinate we should run code 2 to 3 times after both patterns code is completed.
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
- You have seen that the same pattern is repeated. If you count, you will find that pattern is repeated 36 times. So we need a variable `n = 36`.
- According to the rough diagram we should turn turtle upward `t.right(270)` then move 25 pixels `t.forward(25)`.
```python
n = 36                                          
t.right(270)
t.forward(25)
```
![](https://github.com/Sid672/Breakfast_plate/blob/main/bk_7.PNG?raw=true)
- Next, we use loops, the main loop will repeat 36 times because n = 36.
- We fill color in turtle(pen) by `t.fillcolor(col[j])` and change its shape from `arrow --> circle`   after that we print pen shape on paper `t.stamp()`.
- Nested loop repeat `int((3 * n) / 4) = 21 times`.
- Then `t.forward(0.8)`means pen will move 0.8 pixel , `t.left(360/ n)` turn left 10 degrees because `360/ n = 10 degrees`.
- To join the circle and arrow, we require `forward(25)` and change its shape `circle --> arrow` to print it again.
- Similarly, we repeat the next loop in the right direction to achieve a circular path.
- To change the color of the pen use `t.pencolor(color name)`.
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
![](https://github.com/Sid672/Rangoli/blob/main/outer.PNG?raw=true)

# Inner pattern
- It is better to draw inner patterns separately because we can try different combinations with outer patterns.
- First, we set coordinates of the inner part because of the outer pattern our coordinates are not (0, 0).
- So we should correct it. For this we again use `t.up()`, `t.goto(0, 0)` and `t.down()`.
```Python 
t.up()
t.goto(0, 0)
t.down()
```
- Now we change the shape of the pen by `t.shape('arrow')`.
- It's time to decide the shape of the inner pattern for this, we can use triangle, square, rectangle,..... any (n - sided) polygon.
- In this project, we are using a 10 sided polygon. 
- We use a loop to draw a polygon `for i in range(n):` then repeat the same polygon in circular path `for i in range(m):` is used.
- To draw polygon we move `t.forward(24)`, then turn `t.right(360.0/ n)`.
- Again we need some colors so we set `t.pencolor("blue")`.
- To make the pattern more beautiful we fill color in the pen and print(`t.stamp()`) shape of the pen at the edges.
- We should turn the pen, then it will draw the same polygon at different angles. In this way, a circular path is achieved.

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

- In inner design, we need an outline.
- To outline the design we use the same polygon loop but this time without printing pen shape.
- To make the design more interesting we use a different shape of pen `t.shape('turtle')`.
```Python
t.shape('turtle')
for i in range(m): 

  for i in range(n):
    t.pencolor("black")
    t.forward(30)
    t.right(360.0/(n))
    
  t.right(360.0/n)
```
![](https://github.com/Sid672/Rangoli/blob/main/c2.png?raw=true)

# Combination
- We should write both codes together.

### Your code looks like this:
```python
import turtle

#background
s = turtle.Screen()
t = turtle.Turtle()
s.setup(626, 313)
s.bgpic("back.jpg")
t.speed(0)

#colour
col = ["red","orange","yellow","green","blue","purple"]
j = 0
t.pencolor("purple")

#coordinates
t.up()
t.goto(80, -100)
t.down()

#outer pattern:
n = 36
t.right(270)
t.forward(25)
for i in range(n):
   t.fillcolor(col[j])
   t.shape('circle')
   t.stamp()
   for i in range(int((3 * n) / 4)):
       t.forward(0.8)
       t.left(360 / n)
   t.forward(25)
   t.shape('arrow')
   t.stamp()
   for i in range(int((3 * n) / 4)):
        t.forward(0.8)
        t.right(360/ n)
   t.left(10)
   t.forward(25)
   t.pencolor(col[j])
   j = j + 1
   if (j >= 6 ):
      j = 0

#inner pattern:
t.up()
t.goto(0, 0)
t.down()
t.shape('arrow')
n = 10
m = 10

#blue design:
for i in range(m):
   for i in range (n):
       t.forward(24)
       t.right(360.0/(n))
       t.pencolor("blue")
       t.fillcolor("blue")
       t.stamp()
   t.right(360.0/n)
   
#green design:
for i in range (m):
  for i in range(n):
       t.pencolor("green")
       t.fillcolor("green")
       t.forward(26)
       t.left(360.0/(n))
       t.stamp()
  t.left(360.0/n)
  
#red design:
for i in range(m):
   for i in range(n):
       t.pencolor("red")
       t.fillcolor("red")
       t.forward(28)
       t.right(360.0/(n))
       t.stamp()
   t.right(360.0/n)

#outline:
t.shape('turtle')
for i in range(m): 
  for i in range(n):
    t.pencolor("black")
    t.forward(30)
    t.right(360.0/(n))
  t.right(360.0/n)

turtle.done()

```

# Great work!
![](https://media.giphy.com/media/tIeCLkB8geYtW/giphy.gif)


# Links of all demos
### Rangoli
[Code Link](https://repl.it/@Siddharthsing13/rangoli#main.py)
### Variations of  outer pattern
[Code Link](https://repl.it/repls/folder/Rangoli/Variation%20of%20outer%20pattern)
### Variations of the inner pattern
[Code Link](https://repl.it/@Siddharthsing13/v1-1#main.py)

# Happy Hacking:
Now it's your turn to make your Rangoli. You can share your design on [Link](https://hackclub.slack.com/archives/C01504DCLVD). I would love to see your creation. Keep enjoying, keep hacking!
