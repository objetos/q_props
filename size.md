---
weight: 3
draft: false
---

# size

Read-only property that retrieves the quadrille width times the quadrille height.

# Example

{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" width="425" height="425" >}}
`use strict`;
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(int(random(1, 9)), int(random(1, 9)), 15, '🦂');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  text('size: ' + quadrille.size, 20, 20);
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(int(random(1, 9)), int(random(1, 9)), 15, '🦂');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  text('size: ' + quadrille.size, 20, 20);
}
```
{{< /details >}}

# Syntax

> number = quadrille.size