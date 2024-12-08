---
weight: 7
draft: false
title: memory2D
---

Quadrille memory read-write property. TODO always returns a square array where empty cells are filled with `null` (even if they are filled with `undefined` with the memory2D set).

## Example

(mouse click or press any key)  
{{< p5-global-iframe quadrille="true" width="425" height="425" >}}
'use strict';
let quadrille;

function setup() {
  createCanvas(4 * Quadrille.cellLength, 4 * Quadrille.cellLength);
  quadrille = createQuadrille(4, 4);
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
}

function mouseClicked() {
  // property write
  quadrille.memory2D = [
    [150, 100],
    [null, '🫏'],
    [0, 70],
    ['🦂']
  ];
  // property read
  console.log(quadrille.memory2D[quadrille.mouseRow][quadrille.mouseCol]);
}

function keyPressed() {
  // property write
  quadrille.memory2D = ['🫏','🐍', '🦂', '🐵'];
  // property read
  console.log(quadrille.memory2D[quadrille.mouseRow]);
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
let quadrille;

function setup() {
  createCanvas(4 * Quadrille.cellLength, 4 * Quadrille.cellLength);
  quadrille = createQuadrille(4, 4);
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
}

function mouseClicked() {
  // property write
  quadrille.memory2D = [
    [150, 100],
    [null, '🫏'],
    [0, 70],
    ['🦂']
  ];
  // property read
  console.log(quadrille.memory2D[quadrille.mouseRow][quadrille.mouseCol]);
}

function keyPressed() {
  // property write
  quadrille.memory2D = ['🫏','🐍', '🦂', '🐵'];
  // property read
  console.log(quadrille.memory2D[quadrille.mouseRow]);
}
```
{{< /details >}}

## Syntax

> quadrille.memory2D = arr

> arr = quadrille.memory2D