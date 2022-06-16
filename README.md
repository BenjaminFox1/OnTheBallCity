# OnTheBallCity
[VariationOnBouncingBall](https://benjaminfox1.github.io/OnTheBallCity/)
<details><summary>Code Below</summary>
<p>
 
```javascript
 
var dividerW;
var dividerH;

var myFlexiSize;

var myX,myY,speed;


function setup() {
  createCanvas(800,800);
  dividerW = width/20;
  dividerH = height/20;

  myFlexiSize=1;

  myX=50;
  myY=500;
  speedX=4;
  speedY=4;

}

function draw () {
  background(0,166,80);
  fill(255);
  ellipse (myX,myY,50,50);
  noStroke()

for (var i=0; i < 21; i++){
  ellipse(dividerW*i,0,40,40);
  for (var h = 0; h<21; h++) {
    fill(255,242,0);
    ellipse(
      dividerW*i,
      dividerH*h, 
      dist(myX,myY,dividerW*i,dividerH*h)/10+myFlexiSize, 
      dist(myX,myY,dividerW*i,dividerH*h)/10+myFlexiSize);


  fill(0,166,80);
  textSize(70);
  text("On the Ball City!",50,height/2+350)
    
  };
}

myX=myX+speedX;
myY=myY+speedY;

if (myX>width){
  speedX=speedX*-1;
} 

if (myX<0){
  speedX=speedX*-1;
} 

if (myY > height){
  speedY=speedY*-1;
}

if (myY < 0) {
  speedY=speedY*-1;
}

}  

```
</details>
</p>

