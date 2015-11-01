# Pseudo Code for powerup

PROGRAM PowerUpHealth:
  Load programme
  Assign image to file pick
  Create canvas
  Import the image to the canvas in the center position
  Display image
  
  X = loop
  
  WHILE ( X < 4 ):
    Select picture pixels
    Assign picture pixels to canvas pixels
    Make pixels lighter
    Move image allocation up
    Change image displayed
  ENDWHILE
  
    
  WHILE ( X < 4 ):
    Select picture pixels
    Assign picture pixels to canvas pixels
    Make pixels darker
    Move image allocation down
    Change image displayed
  ENDWHILE
    
  Repeat until user presses esc
  Close program

END.
