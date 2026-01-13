---
sidebar_position: 1
title: PCB Layout Essentials
description: Mastering the PCB Editor workspace, design synchronization, and layer management.
---
import useBaseUrl from '@docusaurus/useBaseUrl';


# PCB Layout Essentials

Welcome to the WireFrame PCB Editor. This environment is designed for precision and speed, utilizing hardware-accelerated rendering to handle complex boards smoothly. This section covers the fundamental concepts required to navigate and set up your board layout effectively.

## 1. The Workspace Interface

The PCB Editor is divided into four main zones optimized for an efficient workflow.

![PCB Editor Workspace Overview](/img/Interaface_PBC.png)

* **1. Project struct:** Access common tools like Track Routing, Via Placement, and Zone Filling.
* **2. Design Canvas and toolbar:** The infinite 2D plane where your board layout takes place.
* **3. Library Manager:** Controls visibility and active status of board layers.
* **4. Layer Manager and Properties Panel:** Displays real-time parameters for the currently selected object.

## 2. Synchronizing Design (Schematic to PCB)

Before you can start laying out the board, you need to import the netlist and footprints from your schematic.

### The "Update PCB" Workflow
WireFrame maintains a link between your Schematic Editor and PCB Editor. To transfer changes:

1.  **Open PCB Editor:** Ensure both your Schematic and PCB files are open in the project.
2.  **Trigger Update:** Click the **"Update PCB from Schematic"** icon in the tool in top toolbar.
3.  **Review Changes:** A dialog will appear listing:
    * New components to be added.
    * Netlist connectivity changes.
    * Footprints to be updated.
4.  **Execute:** Click **Update PCB**. The new components will be attached to your cursor for initial placement.

:::warning Component Matching
WireFrame matches components by **Reference Designator** (e.g., R1, U2). If you change a reference in the schematic, ensure you update the PCB to avoid duplicates.
:::


<video controls width="100%">
  <source src={useBaseUrl('/videos/update-pcb-workflow.mp4')} type="video/mp4" />
  Your browser does not support the video tag.
</video>

## 3. Navigation & View Controls

Efficient navigation is critical in PCB design. WireFrame uses standard EDA navigation bindings.

| Action | Mouse / Keyboard Control |
| :--- | :--- |
| **Pan** | Hold **Middle Mouse Button** and drag |
| **Zoom** | Scroll **Mouse Wheel** (Up to zoom in, Down to zoom out) |
| **Zoom to Fit** | Press **Home** key |
| **Flip View** | Press **F** (Flips board view to see from Bottom) |

## 4. Coordinate System & Grids

WireFrame operates on a Cartesian coordinate system.

### Origin Point (0,0)
By default, the origin is at the center of the sheet. You can set a **User Origin** (Spacebar) anywhere to measure relative distances quickly.

### Snap Grid
* **Visual Grid:** The dots or lines you see on the screen.
* **Snap Grid:** The resolution at which your cursor moves.
    * *Shortcut:* Press `G` to cycle through common grid sizes.

## 5. Layer Management

Understanding the Layer Stack is vital. WireFrame uses a color-coded system.

### The "Active Layer" Concept
You can only draw or route on the **Active Layer**.
* **Select a layer** in the Layer Manager to make it active.
* *Shortcut:* Use `Page Up` / `Page Down` to switch active copper layers quickly.

### Standard Layer Types
* **F.Cu / B.Cu (Front/Back Copper):** Signal and power routing layers.
* **F.SilkS / B.SilkS (Silkscreen):** Text, component outlines, and artwork.
* **F.Mask / B.Mask (Solder Mask):** Defines areas where solder mask is removed.
* **Edge.Cuts:** The physical board outline.

## 6. Object Placement & Manipulation

### Moving & Rotating
* **Select:** Click to select a footprint.
* **Move:** Press `M` (or drag) to move.
* **Rotate:** Press `R` to rotate 90° clockwise.

### Flipping (Side Swapping)
To move a component from Top to Bottom (mirroring it):
1.  Select the component.
2.  Press **`F` (Flip)**.
3.  The pads will turn from Red (Front) to Blue (Back).

## Next Steps
* Proceed to **[Routing & Vias](./02-routing)** to start laying down copper.