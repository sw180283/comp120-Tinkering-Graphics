# comp120-Tinkering-Graphics
View raw for indentation.

##Source Code:

  def movePict2():
    src=makePicture("g.jpg")
    canvas=makeEmptyPicture(1000,1000)
    show(canvas)
    targetX=400

    for move in range (0,4):
  
      for i in range(0,4):

       targetY=400   
       for sourceY in range (0,getHeight(src)):
          targetX=400
      
          for sourceX in range (0,getWidth(src)):
            color=getColor(getPixel(src,sourceX,sourceY))
            setColor(getPixel(canvas,targetX,targetY-i*14),color)
            targetX=targetX+1
          targetY=targetY+1
        repaint(canvas)
    
    for down in range (0,4):
      targetY=400-4*14
      for sourceY in range (0,getHeight(src)):
        targetX=400
      
        for sourceX in range (0,getWidth(src)):
          color=getColor(getPixel(src,sourceX,sourceY))
          setColor(getPixel(canvas,targetX,targetY+down*14),color)
          targetX=targetX+1
        targetY=targetY+1
      repaint(canvas)

##Testing:

Start test:

>def makeNewWorld():  
 >  file=pickAFile()  
 >  pic=makePicture(file)  
 >  # I chose to make these two lines so that it is clearer what they are doing.  
  
>   canvas=makeEmptyPicture(400,400)  
>   # Now there is a canvas to import the picture onto.  
>   # I left the colour option blank so it defaults to white.  
  
>   copyInto(pic, canvas, 200,200)  
>   # Put the picture in the center of the canvas.
  
##Notes for next part:
I want the code to make the picture move up and then down, and repeat, as one part of its animation.
I also want to add in some rotation and the copyInto of more pictures.

After trying this, the function didn't work, so I attempted to use a source and target function.

##Start Code
>pic=makeAPicture(pickAFile())  

>canvas=makeEmptyPicture(400,400)  

>targetX=100  

>for sourceX in range(0,getWidth(pic)):  
> targetY=200  
> for sourceY in range(0,getHeight(pic)):  
>  color=getColor(getPixel(pic,sourceX,sourceY)) 
>  setColor(getPixel(canvas,targetX, targetY), color)  
>  targetY=targetY+1  
> #target the next pixel  
> targetX=targetX-1  
>show(pic)  
>show(canvas)  
