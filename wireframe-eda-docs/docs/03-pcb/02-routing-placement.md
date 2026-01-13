---
sidebar_position: 2
title: Routing & Vias
description: Guide to the Interactive Router, placing vias, and managing mechanical holes.
---

import useBaseUrl from '@docusaurus/useBaseUrl';

# Routing & Vias

WireFrame features a modern **Push and Shove Interactive Router**. It is designed to assist you in laying down tracks quickly while automatically enforcing Design Rules (DRC) such as clearance and track width.

## 1. Interactive Routing

To begin routing a track, select the **Route Tbracks** tool from the toolbar or press the hotkey **`X`**.

### Basic Workflow
1.  **Start:** Click on a pad or an existing track to start the trace.
2.  **Guide:** Move the mouse to guide the path. The router will suggest a path based on your cursor position.
3.  **Commit:** Click to fix a segment of the track.
4.  **Finish:** Click on the destination pad to complete the connection.

### Router Modes
WireFrame supports different routing behaviors. You can toggle these in the **Route Menu** or by pressing **`Shift + M`**:

* **Walkaround:** The router will stop when it hits an obstacle and try to go around it.
* **Push and Shove:** The router will move existing tracks and vias out of the way to make room for the new track. *This is the default and recommended mode.*
* **Highlight Collisions:** The router allows you to violate rules but highlights collisions in green/red.

<video controls width="100%">
  <source src={useBaseUrl('/videos/Routing.mp4')} type="video/mp4" />
  Your browser does not support the video tag.
</video>

## 2. Placing Vias (Layer Switching)

Vias are used to connect tracks between different copper layers.

### Placement during Routing
While routing a track (active command `X`):
1.  Press **`V`**.
2.  A via attaches to your cursor.
3.  Click to place the via.
4.  WireFrame automatically switches the active layer (e.g., from Top to Bottom) and continues routing on the new layer.

### Patterned Vias (Stitching)
To place standalone vias (e.g., for Ground Stitching):
1.  Select the **Add Free-standing Vias** tool.
2.  Click on the board to place vias.
3.  **Net Assignment:** Select the via and use the Properties Panel to assign it to a Net (e.g., `GND`).

<video controls width="100%">
  <source src={useBaseUrl('/videos/Via.mp4')} type="video/mp4" />
  Your browser does not support the video tag.
</video>

## 3. Track Widths & Net Classes

You don't need to manually set the width for every track. WireFrame uses **Net Classes** to manage this.

### selecting Track Widths
* **Auto (From Net Class):** The track width is determined by the rules set in *Board Setup > Net Classes* (e.g., Power = 0.5mm, Signal = 0.2mm).
* **Custom Quick-Select:** Use the dropdown in the top toolbar to override the width for specific segments.
* **Shortcut:** Press **`W`** while routing to cycle through pre-defined track widths.

## 4. Mounting Holes & Mechanical Cutouts

Unlike Vias, **Holes** are usually mechanical features (for screws or mounting posts).

### NPTH (Non-Plated Through Hole)
Used for screws where no electrical connection is desired.
1.  Open the **Footprint Library Browser**.
2.  Search for `MountingHole`.
3.  Select a standard size (e.g., `MountingHole_3.2mm_M3`).
4.  Place it on the board.

### PTH (Plated Through Hole)
Used for grounding screws or chassis connections.
1.  Select a `MountingHole_Pad` footprint.
2.  **Assign a Net:** Click on the hole's pad and assign it to `GND` or `Earth` in the Properties Panel.

:::tip Locking Holes
Once you place mounting holes, it is good practice to **Lock** them. Right-click the hole and select **Lock**. This prevents the interactive router or accidental mouse drags from moving them.
:::

<video controls width="100%">
  <source src={useBaseUrl('/videos/Hole.mp4')} type="video/mp4" />
  Your browser does not support the video tag.
</video>

## 5. Editing Traces

Mistakes happen. WireFrame makes it easy to adjust routing without deleting and redrawing.

* **Drag (D):** Hover over a track segment and press `D`. You can push the track line while maintaining connectivity to both ends.
* **Break Track:** Right-click a segment -> *Break Track* to split it into two independent segments.
* **Delete Segment:** Select a segment and press `Del`.
* **Cleanup:** Use **Tools > Remove Unused Tracks** to automatically delete dangling stubs that don't connect to anything.

## Next Steps
Now that your connections are made, proceed to **[Design Rule Check (DRC)](./03-design-rules)** to ensure your board is manufacturable.