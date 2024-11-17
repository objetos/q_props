---
weight: 5
draft: false
title: width
---

Quadrille width read-write property.

## Example

(mouse click or press any key)  
{{< p5-global-iframe quadrille="true" width="425" height="425" >}}
'use strict';
Quadrille.cellLength = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.cellLength, 8 * Quadrille.cellLength);
  quadrille = createQuadrille(int(random(1, 9)), 8);
  quadrille.rand(int(quadrille.size * 0.6), '🐒');
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
  quadrille.rand(int(quadrille.size * 0.6), '🐒');
}

function keyPressed() {
  // property write
  quadrille.width = int(random(1, 9));
  quadrille.rand(int(quadrille.size * 0.6), '🐒');
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
Quadrille.cellLength = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.cellLength, 8 * Quadrille.cellLength);
  quadrille = createQuadrille(int(random(1, 9)), 8);
  quadrille.rand(int(quadrille.size * 0.6), '🐒');
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
  quadrille.rand(int(quadrille.size * 0.6), '🐒');
}

function keyPressed() {
  // property write
  quadrille.width = int(random(1, 9));
  quadrille.rand(int(quadrille.size * 0.6), '🐒');
}
```
{{< /details >}}

## Syntax

> quadrille.width = number

> number = quadrille.width