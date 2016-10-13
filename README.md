# colorWeaver-
ColorWeaver is a digital weaver that works on random variables in the color of the object (line). 

  var a; 
   var offset = 10; 

function setup() {
  createCanvas(1400, 800);
    background(255);
    a = width/2;
    rect(830,15,500,30);
    text("Draw your mouse to a position where you want to see the color spectrum pulled over to.", 850,30);
    text("Enjoy the color flicker that changes every time you reposition your mouse :)",920,40);
    textSize(20);
    stroke(0);
    
    button = createButton("Click to start again!");
  button.position(20,20);
  button.mousePressed(changeText);
  button.class('myButton');
}
 
 function draw() {
   
   if (mouseX > a) { 
     a += 0.5;
     offset = -10; 
 }
 if (mouseX < a) {
   a -= 0.5;
   offset = 10; 
 } 
 if (mouseX < 400) {
   textSize(100);
   stroke(random(255),0,random(255),60);
   text("colorTrick®", 800, 450); 
 } 
 if (mouseX > 1000) {
   textSize(40);
   stroke(random(255),0,random(255),30);
   text("color me :D ", 300, 400); {
     if (mouseX < 500) 
 textSize(40);
   stroke(random(255),0,random(255),60);
     text ("or erase me :(",300,430); 
 }
   }
 
 line(a, 0, a, height); 
 line(mouseX,mouseY,mouseX + offset, mouseY - 10);
 line(mouseX, mouseY, mouseX + offset, mouseY + 10);
 line(mouseX, mouseY, mouseX + offset*3, mouseY);
 }

 

 function changeText() {
  button.html('click again to restart');
  background(255); 
  
}
 

