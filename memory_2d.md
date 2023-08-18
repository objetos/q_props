---
weight: 1
draft: false
---

# memory2D

Quadrille memory read-write property.

# Examples

## Read

(mouse click or press any key and see the console)  
{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" id="number" width="425" height="425" >}}
`use strict`;
let quadrille;
let arr;

function setup() {
  createCanvas(4 * Quadrille.CELL_LENGTH, 4 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(4, 4, 7, 75);
  arr = quadrille.memory2D;
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
}

function mouseClicked() {
  console.log(arr[quadrille.mouseRow][quadrille.mouseCol]);
}

function keyPressed() {
  console.log(arr[quadrille.mouseRow]);
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
let quadrille;
let arr;

function setup() {
  createCanvas(4 * Quadrille.CELL_LENGTH, 4 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(4, 4, 7, 75);
  arr = quadrille.memory2D;
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
}

function mouseClicked() {
  console.log(arr[quadrille.mouseRow][quadrille.mouseCol]);
}

function keyPressed() {
  console.log(arr[quadrille.mouseRow]);
}
```
{{< /details >}}

## Write

(mouse click or press any key)  
{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" id="number" width="425" height="425" >}}
`use strict`;
let quadrille;

function setup() {
  createCanvas(4 * Quadrille.CELL_LENGTH, 4 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(4, 4);
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
}

function mouseClicked() {
  quadrille.memory2D = [
    [150, 100],
    [null, '🫏'],
    [0, 70],
    ['🦂']
  ];
}

function keyPressed() {
  quadrille.memory2D = ['🫏','🐍', '🦂', '🐵'];
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
let quadrille;

function setup() {
  createCanvas(4 * Quadrille.CELL_LENGTH, 4 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(4, 4);
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
}

function mouseClicked() {
  quadrille.memory2D = [
    [150, 100],
    [null, '🫏'],
    [0, 70],
    ['🦂']
  ];
}

function keyPressed() {
  quadrille.memory2D = ['🫏','🐍', '🦂', '🐵'];
}
```
{{< /details >}}

# Syntax

> quadrille.memory2D = arr

> arr = quadrille.memory2D