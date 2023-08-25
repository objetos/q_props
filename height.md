---
weight: 6
draft: false
---

# height

Quadrille height read-write property.

# Example

(mouse click or press any key)  
{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" width="425" height="425" >}}
`use strict`;
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(8, int(random(1, 9)), 15, '🐒');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  // property read
  text('height: ' + quadrille.height, 20, 20);
}

function mouseClicked() {
  // property write
  quadrille.height = int(random(1, 9));
}

function keyPressed() {
  // property write
  quadrille.height = int(random(1, 9));
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(8, int(random(1, 9)), 15, '🐒');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  // property read
  text('height: ' + quadrille.height, 20, 20);
}

function mouseClicked() {
  // property write
  quadrille.height = int(random(1, 9));
}

function keyPressed() {
  // property write
  quadrille.height = int(random(1, 9));
}
```
{{< /details >}}

# Syntax

> quadrille.height = number

> number = quadrille.height