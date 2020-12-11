[Home](README.md) | [Beginner Python Turtle Graphics](Turtle.md) | [Recursive Python Turtle Graphics](Recursive.md) | [SVG Graphics](SVG.md) | [Paint Job Estimator](Paint.md)

## Beginner Python Turtle Graphics

#### Overview

The [Python Turtle Graphics](https://docs.python.org/3/library/turtle.html) module allows programmers to created two-dimensional images from commands. In this project I had to create any image that I wanted, as long as it used Python turtle Graphics. I had already had some experience with the graphics, so doing this assignment was not very difficult. I chose a frog as the subject because my girlfriend really likes frogs.



![Turtle Image](https://davidjlu.github.io/CCUT/CS161/House.png)



#### History

As stated form the [Python Documentation](https://docs.python.org/3/library/turtle.html): "Turtle graphics is a popular way for introducing programming to kids. It was part of the original Logo programming language developed by Wally Feurzeig, Seymour Papert and Cynthia Solomon in 1967. The turtle module is an extended reimplementation of the same-named module from the Python standard distribution up to version Python 2.5. It tries to keep the merits of the old turtle module and to be (nearly) 100% compatible with it. The turtle module provides turtle graphics primitives, in both object-oriented and procedure-oriented ways"



Turtle Graphics are useful in creating:

- Logos

- Basic Graphics

- Animations

- Games



#### Programming Project

The INFOTC 1040 Python Turtle Graphics challenge states: In this programming challenge you are to create a Python program called turtleimage.py that uses Turtle graphics to draw a graphic image. The image you draw is up to you. Visualize a graphic image you want to create, then try to create it in Python using Turtle graphics. The goal of this challenge is to write a basic Python program that uses Turtle graphics.



Below is a screenshot of the program in action.

![Image of Screenshot](Pictures/turtle.jpg)



This is the code for the program:


```python
import turtle

#Setup
turtle.title("Froggie")
turtle.bgcolor('#ffe53b')
t = turtle
turtle.speed(5000)

#Frog Head
t.penup()
t.goto(-100,-110)
t.pencolor("green")
t.pensize(200)
t.pendown()
t.fd(200)
t.pencolor("black")
t.pensize(1)
t.penup()

#Frog Smile
t.goto(-100,-100)
t.pencolor("black")
t.pensize(20)
t.rt(25)
t.pendown()
t.fd(25)
t.lt(15)
t.fd(75)
t.lt(20)
t.fd(75)
t.lt(10)
t.fd(25)
t.pencolor("black")
t.pensize(1)
t.rt(25)
t.penup()

#Frog Tongue
t.lt(20)
t.goto(10,-130)
t.fillcolor("red") 
t.begin_fill() 
for j in range(4): 
    t.forward(30) 
    t.right(90) 
t.end_fill() 
t.penup()
t.rt(25)
t.goto(30,-170)
t.fillcolor("red") 
t.begin_fill() 
t.circle(15) 
t.end_fill() 
t.penup()

#Right Green Eyelid
t.penup()
t.goto(90,0)
t.pendown()
t.color("green")
t.dot(120)
t.penup()

#Left Green Eyelid
t.goto(-90,0)
t.pendown()
t.color("green")
t.dot(120)
t.penup()

#Eye Connector
t.goto(-40,-17)
t.pendown()
t.fd(100)
t.penup()
t.goto(7,-17)
t.pendown()
t.lt(350)

#Eye Connector Triangles
t.fillcolor("green") 
t.begin_fill() 
for _ in range(3): 
    t.forward(50) 
    t.right(-120) 
t.end_fill() 
t.penup()
t.lt(60)
t.goto(-7,-17)
t.pendown()
t.lt(95)
t.fillcolor("green") 
t.begin_fill() 
for _ in range(3): 
    t.forward(50) 
    t.right(-120) 
t.end_fill() 
t.penup()
t.lt(230)

#Right Eyeball
t.goto(95,0)
t.pendown()
t.color("orange")
t.dot(100)
t.color("black")
t.dot(80)
t.penup()

#Right Eye Glint
t.fd(10)
t.lt(90)
t.fd(10)
t.color("white")
t.pendown()
t.dot(20)
t.penup()
t.lt(90)
t.fd(25)
t.lt(90)
t.fd(30)
t.pendown()
t.dot(10)
t.penup()

#Left Eyeball
t.goto(-95,0)
t.pendown()
t.color("orange")
t.dot(100)
t.color("black")
t.dot(80)
t.penup()

#Left Eye Glint
t.goto(-110,10)
t.color("white")
t.pendown()
t.dot(20)
t.penup()
t.goto(-85,-20)
t.pendown()
t.dot(10)
t.penup()

#Nose
t.goto(20,-60)
t.pendown()
t.color("black")
t.dot(20)
t.penup()
t.goto(-20,-60)
t.pendown()
t.color("black")
t.dot(20)
t.penup()

#Turtle
t.goto(0,150)
t.lt(130)
t.fillcolor("green")
t.shapesize(5,5,5)
t.shape("turtle")
t.end_fill()

#Exit
try:
    t.exitonclick()  # or mainloop() or done()
except Exception:
    pass

```



*This website was created in Markdown for Garrett High's Introduction to Information Technology class as a final project in the 2020 Fall Semester*