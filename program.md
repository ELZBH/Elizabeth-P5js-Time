##Code as written on p5js. Accessed at: https://editor.p5js.org/ELZBH/sketches/eCMbibN8W##

let pos = 0
let pos1 = 5
let pos2 = 10
let pos3 = 20
let pos4 = 40
let round = 0
let swap = 0

function setup() {
  createCanvas(300, 300);
  background(25, 35, 45);
  frameRate(15);
}

function draw() {
  if(swap>0 && random(1,9)<5){
    fill(random(0,255),random(0,255),random(0,255))
  }
  triangle(pos,pos,pos,pos3,pos2,pos);
  triangle(pos,pos3,pos,pos4,pos2,pos4);
  triangle(pos1,pos,pos2,pos,pos1,pos3);
  triangle(pos1,pos4,pos2,pos4,pos1,pos3);
  if(pos<20){
    pos = pos + 1
  }else{
    pos = pos + 4
  }
  pos1 = pos1 + 5
  pos2 = pos2 + 10
  pos3 = pos3 + 20
  pos4 = pos4 + 40
  if(swap>0 && swap%random(1,2)==0){
    fill(random(0,255),random(0,255),random(0,255))
  }
  if(pos==300 && round%2==0){
    erase()
    pos = 0
    pos1 = 5
    pos2 = 10
    pos3 = 20
    pos4 = 40
    round = round + 1
  }
  if(pos>85 && round%2==1){
    noErase()
    pos = 0
    pos1 = 5
    pos2 = 10
    pos3 = 20
    pos4 = 40
    round = round + 1
    swap = swap + 1
    fill(random(0,255),random(0,255),random(0,255))
  }
  
}
