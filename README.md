# doth
ballx=100
bally=100
ballxspeed=0
ballyspeed=0
r2=250
f2=250

def setup():
    global ballx,bally
    size(800,600)
    ballx=width/2
    bally=height/2
def draw():
    global ballx,bally,ballxspeed,ballyspeed,f2,r2
    fill(51,255,255)
    rect(100,100,600,400)
    fill(0,0,0)
    rect(140,r2,10,100)
    if keyPressed:
        if key == 'w' and r2>=101:
            r2-=5
        if key == 's' and r2<=399:
            r2+=5
        if key == 'p':
              ballxspeed=+5
              ballyspeed=-5
    fill(255,255,255)   
    rect(660,f2,10,100 )
    if keyPressed:
        if key == 'o' and f2>=101:
            f2-=5
        if key == 'l' and f2<=399:
            f2+=5
    line(400,100,400,500)
    fill(0,0,255)
    triangle(400,150,350,100,450,100)
    fill(255,0,0)
    triangle(400,450,350,500,450,500)
    ellipse(ballx,bally,10,10)
    ballx+=ballxspeed
    bally+=ballyspeed
    if ballx<=150 and bally>=r2 and bally<=r2+100 and ballx>=140 :
            ballxspeed=-ballxspeed
    if ballx>=650 and bally>=f2 and bally<=f2+100 and ballx<=660: 
            ballxspeed=-ballxspeed
    if ballx<=106:
       ballxspeed=-ballxspeed
    if bally>=494:
       ballyspeed=-ballyspeed
    if bally<=106:
       ballyspeed=-ballyspeed
    if ballx>=694:
       ballxspeed=-ballxspeed
    if ballx<=100:
        ballxspeed=0
        ballyspeed=0
        ballx=100
        bally=100
    if ballx>=700:
        ballxspeed=0
        ballyspeed=0
        ballx=100
        bally=100

       
     
       
   
