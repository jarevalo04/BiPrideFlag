# BiPrideFlag
/*Bisexual Pride: Jose A. Kenia E. Period 5*/
/*Postconditions: Karel is at the start of the world
with no knowledge of the functions that will be used*/
/*Karel will paint a Bisexual Pride Flag on a 20x20 canvas*/
/*Optional,Karel can paint a mini version on the 40x40 canvas*/
function start(){
    //Karel moves to the "corner" of the flag//
    moveToStartCorner();
    //Karel uses commands like "paintpride" followed by the 
    //color to paint the colors of the flag//
    for(var i=0; i<2; i++){
        paintPrideBlue();
    }
    paintPridePurple();
    //lrowturn or "left" row turn is created to have karel turn 
    //after painting a row of paint to move onto the next row easier
    lRowTurn();
    for(var i=0; i<2; i++){
        paintPrideMagenta();
    }
    //Karel moves back to the left but at the same row that 
    //karel finished painting the magenta color//
    moveToEnd();
    //Using functions that karel has learned, Karel will spell
    //pride out aswell as in color//
    pForPride();
    rForPride();
    iForPride();
    dForPride();
    eForPride();
}
//this function is designed to paint the blue portion of the flag//
function paintPrideBlue(){
    paint(Color.createFromRGB(0,56,168));
    move();
     for(var i=0; i<17; i++){
        paint(Color.createFromRGB(0,56,168));
        move();
    }
    lRowTurn();
    paint(Color.createFromRGB(0,56,168));
    move();
     for(var i=0; i<17; i++){
        paint(Color.createFromRGB(0,56,168));
        move();
    }
    rRowTurn();
}
//this function is designed to paint the middle purple portion
//of the flag//
function paintPridePurple(){
    paint(Color.createFromRGB(155,79,150));
    move();
     for(var i=0; i<17; i++){
        paint(Color.createFromRGB(155,79,150));
        move();
    }
    lRowTurn();
    paint(Color.createFromRGB(155,79,150));
    move();
     for(var i=0; i<17; i++){
        paint(Color.createFromRGB(155,79,150));
        move();
    }
    rRowTurn();
    paint(Color.createFromRGB(155,79,150));
    move();
     for(var i=0; i<17; i++){
        paint(Color.createFromRGB(155,79,150));
        move();
    }
}
//this function is designed to paint the magneta portion of 
//the flag//
function paintPrideMagenta(){
    paint(Color.createFromRGB(214,2,112));
    move();
     for(var i=0; i<17; i++){
        paint(Color.createFromRGB(214,2,112));
        move();
    }
    rRowTurn();
    paint(Color.createFromRGB(214,2,112));
    move();
     for(var i=0; i<17; i++){
        paint(Color.createFromRGB(214,2,112));
        move();
    }
    lRowTurn();
}
//this function is designed to move karel to the start 
//by placing her to a corner of the soon to be flag//
function moveToStartCorner(){
    move();
    turnLeft();
    move();
    turnRight();
}
// a turn function designed have karel turn left smoothly onto 
//the next row//
function lRowTurn(){
    turnLeft();
    move();
    turnLeft();
    move();
}
//another turn function used when karel is turning right 
//onto the next row//
function rRowTurn(){
    turnRight();
    move();
    turnRight();
    move();
}
//a function used to have karel move from the end of the paintpride
//magenta command to the very left preparing to spell pride
function moveToEnd(){
    for(var i=0; i<18; i++){
        move();
    }
}
//These next set of functions are designed to have karel paint
//the word pride out ontop of the flag//
function pForPride(){
    turnRight();
    move();
    turnRight();
    move();
    paint(Color.createFromRGB(214,2,112));
    turnLeft();
    for(var i=0; i<5; i++){
        move();
        paint(Color.createFromRGB(214,2,112));
    }
    turnRight();
    for(var i=0; i<3; i++){
        move();
        paint(Color.createFromRGB(214,2,112));
    }
    turnRight();
    for(var i=0; i<3; i++){
        move();
        paint(Color.createFromRGB(214,2,112));
    }
    turnRight();
    for(var i=0; i<2; i++){
        move();
        paint(Color.createFromRGB(214,2,112));
    }
}
function rForPride(){
    turnLeft();
    move();
    move();
    turnLeft();
    for(var i=0; i<3; i++){
        move();
    }
    paint(Color.createFromRGB(155,79,150));
    turnLeft();
    for(var i=0; i<2; i++){
        move();
        paint(Color.createFromRGB(155,79,150));
    }
    turnRight();
    for(var i=0; i<2; i++){
        move();
        paint(Color.createFromRGB(155,79,150));
    }
}
function iForPride(){
    turnRight();
    move();
    move();
    turnLeft();
    move();
    turnLeft();
    for(var i=0; i<3; i++){
        paint(Color.createFromRGB(0,56,168));
        move();
    }
    move();
    paint(Color.createFromRGB(0,56,168));
    move();
}
function dForPride(){
    turnRight();
    for(var i=0; i<4; i++){
        move();
    }
    turnRight();
    for(var i=0; i<5; i++){
        paint(Color.createFromRGB(214,2,112));
        move();
    }
    turnRight();
    for(var i=0; i<3; i++){
        paint(Color.createFromRGB(214,2,112));
        move();
    }
    turnRight();
    for(var i=0; i<2; i++){
        paint(Color.createFromRGB(214,2,112));
        move();
    }
    turnRight();
    for(var i=0; i<3; i++){
        paint(Color.createFromRGB(214,2,112));
        move();
    }
}
function eForPride(){
    for(var i=0; i<3; i++){
        move();
        paint(Color.createFromRGB(155,79,150));
    }
    turnRight();
    move();
    move();
    paint(Color.createFromRGB(155,79,150));
    turnRight();
    for(var i=0; i<2; i++){
        paint(Color.createFromRGB(155,79,150));
        move();
    }
    turnRight();
    paint(Color.createFromRGB(155,79,150));
    move();
    paint(Color.createFromRGB(155,79,150));
    for(var i=0; i<3; i++){
        move();
        paint(Color.createFromRGB(155,79,150));
    }
    turnRight();
    for(var i=0; i<2; i++){
        move();
        paint(Color.createFromRGB(155,79,150));
    }
}
