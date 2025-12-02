---
weight: 5
draft: false
title: span
---

Gets the minimal axis-aligned span of filled cells as the object `{row, col, width, height}`. Returns `undefined` if the quadrille has no filled cells.

## Example

(mouse click to toggle emojis; press any key to randomizechange quadrille order & size)  
{{< p5-global-iframe quadrille="true" width="475" height="325" >}}
'use strict';

Quadrille.cellLength = 30;

let p, q;
let span;

function setup() {
  createCanvas(15 * Quadrille.cellLength, 10 * Quadrille.cellLength);
  q = createQuadrille(15, 10, 8, '😼');
  reset();
}

function draw() {
  background('BlueViolet');
  drawQuadrille(q);
  drawQuadrille(p, { col: span.col, row: span.row, outline: 'yellow' });
}

function mouseClicked() {
  const row = q.mouseRow;
  const col = q.mouseCol;
  if (q.isValid(row, col)) {
    q.isFilled(row, col) ? q.clear(row, col) : q.fill(row, col, '🐦');
    reset();
  }
}

function keyPressed() {
  q.randomize();
  reset();
}

function reset() {
  span = q.span;
  p = createQuadrille(span.width, span.height);
}
{{< /p5-global-iframe >}}

{{% details title="code" open=true %}}
```js
Quadrille.cellLength = 30;

let p, q;
let span;

function setup() {
  createCanvas(15 * Quadrille.cellLength, 10 * Quadrille.cellLength);
  q = createQuadrille(15, 10, 8, '😼');
  reset();
}

function draw() {
  background('BlueViolet');
  drawQuadrille(q);
  drawQuadrille(p, { col: span.col, row: span.row, outline: 'yellow' });
}

function mouseClicked() {
  const row = q.mouseRow;
  const col = q.mouseCol;
  if (q.isValid(row, col)) {
    q.isFilled(row, col) ? q.clear(row, col) : q.fill(row, col, '🐦');
    reset();
  }
}

function keyPressed() {
  q.randomize();
  reset();
}

function reset() {
  span = q.span;
  p = createQuadrille(span.width, span.height);
}
```
{{% /details %}}

## Syntax

> number = quadrille.span
