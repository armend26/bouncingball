#Bouncing Ball V1.0
import turtle 
import random 

#window 
wn = turtle.Screen() 
wn.title("Bouncing Ball v1.0") 
wn.bgcolor("white") 
wn.cv._rootwindow.resizable(False, False)
wn.tracer(0) 

#score 
score = 0 

#ball 
ball = turtle.Turtle() 
ball.speed(0) 
ball.shape("circle") 
ball.color("blue") 
ball.penup() 
ball.goto(0,0)
ball.dx = 0.1
ball.dy = 0.1


#borders_x
border_x_right = turtle.Turtle()
border_x_right.speed(0)
border_x_right.shape("square")
border_x_right.color("black") 
border_x_right.shapesize(stretch_wid=28,stretch_len=0.1)
border_x_right.penup() 
border_x_right.goto(325,0)

border_x_left = turtle.Turtle()
border_x_left.speed(0)
border_x_left.shape("square")
border_x_left.color("black") 
border_x_left.shapesize(stretch_wid=28,stretch_len=0.1)
border_x_left.penup() 
border_x_left.goto(-325,0)

#borders_y
border_y_right = turtle.Turtle()
border_y_right.speed(0)
border_y_right.shape("square")
border_y_right.color("black") 
border_y_right.shapesize(stretch_wid=0.1,stretch_len=32.5)
border_y_right.penup() 
border_y_right.goto(0,276)

border_y_left = turtle.Turtle()
border_y_left.speed(0)
border_y_left.shape("square")
border_y_left.color("black") 
border_y_left.shapesize(stretch_wid=0.1,stretch_len=32.5)
border_y_left.penup() 
border_y_left.goto(0,-276)


#colors 
color = ["red","black","green","purple","yellow"] 

#bordercheck
def border_x_check(x):
	ball.color(random.choice(color))
	ball.dx *= -1
	if x>0: 
		border_x_right.color(random.choice(color))

	else: 
		border_x_left.color(random.choice(color))
 
def border_y_check(y):
	ball.color(random.choice(color))
	ball.dy *= -1
	if y>0:
		border_y_right.color(random.choice(color))
	else: 
		border_y_left.color(random.choice(color))

#pen 
pen = turtle.Turtle() 
pen.speed(0)
pen.shape("square")
pen.color("black")
pen.penup()
pen.hideturtle()
pen.goto(0, 0)

#credits  
credits = turtle.Turtle()
credits.speed(0)
credits.shape("square") 
credits.color("black")
credits.hideturtle() 
credits.goto(0,0)
credits.write("Created by Armend Ostaku",align="center",font=("Courier",10,"normal"))


#main 
while True:
	wn.update()
	ball.setx(ball.xcor()+ball.dx)
	ball.sety(ball.ycor()+ball.dy)
	if ball.xcor() > 315 or ball.xcor() < -315:
		border_x_check(ball.xcor())
		score+=1
		pen.clear()
		pen.write("{}".format(score), align="center", font=("Courier", 60, "normal"))

	if ball.ycor() > 265 or ball.ycor() < -265: 
		score+=1
		border_y_check(ball.ycor())
		pen.clear()
		pen.write("{}".format(score), align="center", font=("Courier", 60, "normal"))
