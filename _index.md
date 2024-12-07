---
bookCollapseSection: true  
weight: 3  
draft: false  
---

# Properties  

The `Quadrille` object offers a set of **properties** that are categorized into **read-only** and **read/write** groups. These properties allow you to inspect or modify the state and behavior of a quadrille.  

### Read-Only Properties  
Read-only properties provide insights into the quadrille's current state and cannot be directly modified:  
- **[mouseRow]({{< relref "mouse_row" >}}):** The row index of the cell currently under the mouse pointer.  
- **[mouseCol]({{< relref "mouse_col" >}}):** The column index of the cell currently under the mouse pointer.  
- **[size]({{< relref "size" >}}):** The total number of cells in the quadrille.  
- **[order]({{< relref "order" >}}):** The number of rows and columns in the quadrille (assumes a square layout).

### Read/Write Properties  
Read/write properties can be both accessed and modified, allowing dynamic control over the quadrille's dimensions and content:  
- **[width]({{< relref "width" >}}):** The number of columns in the quadrille.  
- **[height]({{< relref "height" >}}):** The number of rows in the quadrille.  
- **[memory2D]({{< relref "memory_2d" >}}):** A 2D array that represents the content of each cell.  

Access and modify these properties using **dot notation**, a standard approach in JavaScript for working with object properties.  

By combining these properties, you can efficiently read the quadrille's state and customize its structure to suit your needs.  