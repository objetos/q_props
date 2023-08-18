---
weight: 5
draft: false
---

# width

Quadrille width read-write property.

# Example

(mouse click or press any key)  
{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" id="number" width="425" height="425" >}}
`use strict`;
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(int(random(1, 9)), 8, 15, '🐒');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  // property read
  text('width: ' + quadrille.width, 20, 20);
}

function mouseClicked() {
  // property write
  quadrille.width = int(random(1, 9));
}

function keyPressed() {
  // property write
  quadrille.width = int(random(1, 9));
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(int(random(1, 9)), 8, 15, '🐒');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  // property read
  text('width: ' + quadrille.width, 20, 20);
}

function mouseClicked() {
  // property write
  quadrille.width = int(random(1, 9));
}

function keyPressed() {
  // property write
  quadrille.width = int(random(1, 9));
}
```
{{< /details >}}

# Syntax

> quadrille.width = number

> number = quadrille.width