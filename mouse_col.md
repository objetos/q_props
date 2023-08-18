---
weight: 2
draft: false
---

# mouseCol

Read-only property that retrieves the quadrille col under the current mouse position.

{{< hint warning >}}
**Observation**  
The `mouseCol` property isn't constrain to lie in [0..[width]({{< ref "width" >}})].
{{< /hint >}}

# Example

{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" id="number" width="425" height="425" >}}
`use strict`;
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(int(random(1, 9)), int(random(1, 9)));
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  text('mouseCol: ' + quadrille.mouseCol, 20, 20);
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
Quadrille.CELL_LENGTH = 50;
let quadrille;

function setup() {
  createCanvas(8 * Quadrille.CELL_LENGTH, 8 * Quadrille.CELL_LENGTH);
  quadrille = createQuadrille(int(random(1, 9)), int(random(1, 9)));
}

function draw() {
  background('#6495ED');
  drawQuadrille(quadrille);
  text('mouseCol: ' + quadrille.mouseCol, 20, 20);
}
```
{{< /details >}}

# Syntax

> number = quadrille.mouseCol