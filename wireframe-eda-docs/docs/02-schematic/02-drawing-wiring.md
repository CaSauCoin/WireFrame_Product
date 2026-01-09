---
sidebar_position: 2
title: Drawing & Wiring
description: Master the tools for connecting components, drawing shapes, and modifying object properties.
---

# Drawing & Wiring Tools

Once your components are placed on the canvas, the next step is to connect them electrically and arrange them logically. This section covers the essential tools for wiring, graphic drawing, and object manipulation.

## 1. Wiring components (The "W" Tool)

The **Wire** tool is the most used feature in the schematic editor. It creates electrical connections (nets) between component pins.

### How to place a wire:
1.  Press `W` or click the **Wire** icon <img src="/img/wire_icon.png" width="20"/> on the toolbar.
2.  Hover over a component pin until you see the **snap indicator** (usually a small circle or crosshair).
3.  **Click** to start the wire.
4.  Move the mouse to the destination pin and **Click** again to finish.

:::tip[Auto-Junctions]
When a wire crosses and connects to another existing wire (T-junction), WireFrame automatically places a **Junction Dot** to indicate an electrical connection. Crossing wires without dots are *not* connected.
:::

<video controls width="100%">
  <source src="/videos/Wires.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>
---

## 2. Selection modes

Efficient editing starts with selecting exactly what you want. WireFrame supports two primary selection modes using the **Select Tool** (`Esc`).

| Mode | Action | Description |
| :--- | :--- | :--- |
| **Single Select** | Click | Click directly on a component, wire, or text to select it. |
| **Box Select** | Click & Drag | Click on empty space and drag to create a selection rectangle. |
| **Add to Selection** | `Ctrl` + Click | Hold `Ctrl` while clicking to add multiple items to the current selection. |

> **[PLACEHOLDER GIF: selection-modes.gif]**
> *Description: Show clicking a single resistor (it highlights). Then show dragging a large box around the whole circuit to select everything.*

---

## 3. Graphic primitives

Sometimes you need to add non-electrical drawings, such as borders, separation lines, or notes. These objects **do not** appear in the netlist or PCB.

To access these tools, look for the **Graphics** dropdown on the toolbar or use the shortcut `G`.

* **Line / Polyline:** Draw straight lines or polygons.
* **Rectangle / Circle:** Draw closed shapes for grouping sections.
* **Text:** Add annotations or instructions (e.g., *"Power Input Section"*).

:::info[Visualizing Logic]
Use graphic rectangles with dashed lines to group related circuit blocks (e.g., Power, MCU, Sensors) to make your schematic readable for other engineers.
:::

> **[PLACEHOLDER IMAGE: graphics-example.png]**
> *Description: Screenshot of a schematic section where a Dashed Rectangle surrounds a power circuit, with a text label saying "5V Regulator".*

---

## 4. Object manipulation

Modify your design layout using standard transformation tools.

### Move & Rotate
* **Move:** Select an object and drag it with the mouse, or press `M`. Connected wires will stretch to maintain connectivity (Rubber-banding).
* **Rotate:** While an object is selected (or while moving it), press `Space` or `R` to rotate it 90 degrees clockwise.

### Copy & Delete
* **Copy/Paste:** Standard `Ctrl + C` and `Ctrl + V` work for single items or entire circuit blocks.
* **Delete:** Press `Delete` or `Backspace` to remove selected items.

> **[PLACEHOLDER GIF: move-rotate.gif]**
> *Description: Select a component. Drag it around (wires stretching). While dragging, press Spacebar to rotate it.*

---

## 5. Changing properties

Every object in WireFrame has attributes you can edit.

1.  Select the object (e.g., a Resistor).
2.  Look at the **Properties Panel** on the right side.
3.  Update the values directly.

**Common editable properties:**
* **Value:** Change `1k` to `10k`.
* **Designator:** Change `R?` to `R1`.
* **Attributes:** Toggle visibility of specific text fields (e.g., hide the Pin Numbers if the symbol is too cluttered).

> **[PLACEHOLDER IMAGE: properties-panel-edit.png]**
> *Description: Split image. Left side: The resistor on canvas showing "1k". Right side: The Properties Panel with "Value: 10k" being typed in.*