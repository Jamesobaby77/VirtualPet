void setup() {
  size(800, 600);
  background(255);
  
  // Draw a cat
  drawCat(150, 300, 150, 100);
  
  // Draw a fish
  drawFish(550, 300, 150, 70);
}

void drawCat(float x, float y, float w, float h) {
  // Body
  fill(200, 150, 100);
  ellipse(x, y, w, h);
  
  // Head
  ellipse(x, y - h/2 - w/4, w/2, w/2);
  
  // Eyes
  fill(0);
  ellipse(x - w/8, y - h/2 - w/4, w/10, w/10);
  ellipse(x + w/8, y - h/2 - w/4, w/10, w/10);
  
  // Nose
  fill(255, 100, 100);
  triangle(x, y - h/2 - w/4 + 10, x - 5, y - h/2 - w/4 + 20, x + 5, y - h/2 - w/4 + 20);
  
  // Ears
  fill(200, 150, 100);
  triangle(x - w/4, y - h/2 - w/4, x - w/8, y - h/2 - w/2, x, y - h/2 - w/4);
  triangle(x + w/4, y - h/2 - w/4, x + w/8, y - h/2 - w/2, x, y - h/2 - w/4);
  
  // Tail
  stroke(200, 150, 100);
  strokeWeight(10);
  line(x + w/2, y, x + w, y - h/4);
  
  noStroke();
}

void drawFish(float x, float y, float w, float h) {
  // Body
  fill(100, 150, 200);
  ellipse(x, y, w, h);
  
  // Tail
  triangle(x - w/2, y, x - w/2 - w/4, y - h/4, x - w/2 - w/4, y + h/4);
  
  // Eye
  fill(0);
  ellipse(x + w/4, y - h/8, w/10, w/10);
  
  // Fin
  fill(100, 150, 200);
  triangle(x + w/8, y, x + w/2, y - h/4, x + w/2, y + h/4);
}
