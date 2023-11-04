---
bookCollapseSection: true
weight: 3
draft: false
---

# Properties

`Quadrille` properties are divided into read-only and read/write categories. Read-only properties include [mouseRow]({{< relref "mouse_row" >}}), [mouseCol]({{< relref "mouse_col" >}}), [size]({{< relref "size" >}}), and [order]({{< relref "order" >}}), which provide insights into the quadrille's state. On the other hand, [width]({{< relref "width" >}}), [height]({{< relref "height" >}}), and [memory2D]({{< relref "memory_2d" >}}) can be both read and set. Access and assign these properties using [dot notation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors#dot_notation), for example: `let order = quadrille.order;` or `quadrille.width = 5;`.