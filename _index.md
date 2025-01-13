---
bookCollapseSection: true  
weight: 3  
title: Properties
draft: false  
---

The **Quadrille** object includes a robust set of **properties** designed to facilitate both state inspection and dynamic configuration. These properties are neatly divided into **read-only** and **read/write** categories, offering intuitive control over the quadrille's behavior and layout. The read-only properties provide valuable insights, while the read/write properties enable direct modifications to shape and content.

### **Read-Only Properties**  
[Read-only properties]({{< relref "read_only" >}}) allow you to inspect the quadrille's current state without altering it. For example, **[mouseRow]({{< relref "mouse_row" >}})** and **[mouseCol]({{< relref "mouse_col" >}})** identify the cell under the mouse pointer, while **[size]({{< relref "size" >}})** and **[order]({{< relref "order" >}})** offer details on the quadrille's total and non-empty cells.

### **Read/Write Properties**  
In contrast, [read/write properties]({{< relref "read_write" >}}) let you dynamically adjust the quadrille's configuration. For instance, **[width]({{< relref "width" >}})** and **[height]({{< relref "height" >}})** control the quadrille's dimensions, while **[memory2D]({{< relref "memory_2d" >}})** provides a complete 2D representation of its content, enabling full customization.

These properties can be easily accessed and manipulated using JavaScript's **dot notation**, making them versatile tools for managing a quadrille's state and structure.