---
weight: 4
draft: false
title: order
---

# order

Read-only property that retrieves the quadrille non-empty number of cells.

# Example

{{< p5-global-iframe quadrille="true" width="425" height="425" >}}
`use strict`;
Quadrille.cellLength = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.cellLength, 8 * Quadrille.cellLength);
  quadrille = createQuadrille(int(random(1, 9)), int(random(1, 9)), int(random(5, 30)), '🐍');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  text('order: ' + quadrille.order, 20, 20);
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
Quadrille.cellLength = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.cellLength, 8 * Quadrille.cellLength);
  quadrille = createQuadrille(int(random(1, 9)), int(random(1, 9)),
                              int(random(5, 30)), '🐍');
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  text('order: ' + quadrille.order, 20, 20);
}
```
{{< /details >}}

# Syntax

> number = quadrille.order