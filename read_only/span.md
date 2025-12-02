---
weight: 5
draft: false
title: span
---

Gets the smallest axis-aligned rectangle that contains all filled cells. Returns an object of the form `{ row, col, width, height }`, or `undefined` if the quadrille is entirely empty.

## Example

(mouse click to toggle emojis; press any key to randomize the quadrille)  
{{< p5-global-iframe quadrille="true" width="475" height="325" >}}
'use strict';

Quadrille.cellLength = 30;

let p, q;
let span;

function setup() {
  createCanvas(15 * Quadrille.cellLength, 10 * Quadrille.cellLength);
  q = createQuadrille(15, 10, 8, '😼');
  update();
}

function draw() {
  background('BlueViolet');
  drawQuadrille(q);
  span && drawQuadrille(p, { col: span.col, row: span.row, outline: 'yellow' });
}

function mouseClicked() {
  const row = q.mouseRow;
  const col = q.mouseCol;
  if (q.isValid(row, col)) {
    q.isFilled(row, col) ? q.clear(row, col) : q.fill(row, col, '🐦');
    update();
  }
}

function keyPressed() {
  q.randomize();
  update();
}

function update() {
  span = q.span;
  p = span && createQuadrille(span.width, span.height);
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
  update();
}

function draw() {
  background('BlueViolet');
  drawQuadrille(q);
  span && drawQuadrille(p, { col: span.col, row: span.row, outline: 'yellow' });
}

function mouseClicked() {
  const row = q.mouseRow;
  const col = q.mouseCol;
  if (q.isValid(row, col)) {
    q.isFilled(row, col) ? q.clear(row, col) : q.fill(row, col, '🐦');
    update();
  }
}

function keyPressed() {
  q.randomize();
  update();
}

function update() {
  span = q.span;
  p = span && createQuadrille(span.width, span.height);
}
```
{{% /details %}}

## Syntax

> number = quadrille.span
