---
sidebar_position: 1
title: Interface & Project Management
description: Get familiar with the workspace, MDI tab system, and project file management.
---

# Interface & Project Management

Welcome to **WireFrame Schematic Editor**—the starting point for every electronics design. This page helps you get familiar with the workspace, file organization, and a few essential initial settings.

## 1. Workspace overview

WireFrame’s UI is intentionally minimal and focused on the design area. It is organized into four main regions:

:::info[Main regions]
1.  **Top toolbar:** Drawing tools, grid controls, and settings.
2.  **Project Explorer (left):** Manages the project’s file tree.
3.  **Properties panel (right):** Edits properties of the currently selected object.
4.  **Design canvas (center):** The main schematic drawing area with an MDI tab system.
:::

![Interface](/img/Interface.jpg)
---

## 2. Project structure

WireFrame organizes designs using a strict tree structure to help maintain data integrity. A typical project includes the following file types:

| File type | Extension | Description |
| :--- | :--- | :--- |
| **Project file** | `.prjxml` | Root file containing project-wide configuration. |
| **Schematic** | `.schxml` | Schematic capture (logical design). |
| **PCB layout** | `.pcbxml` | PCB layout (board design). |

### Working with files
You can manage files directly from the **Project Explorer** panel:

* **Create:** Right-click the project → New Schematic/PCB.
<video controls width="100%">
  <source src="/videos/Create_Schematic.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>

* **Move:** Drag and drop to reorder (if supported).
<video controls width="100%">
  <source src="/videos/import_lib.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>
---

## 3. Multi-tab system (MDI)

WireFrame supports multitasking via an MDI (Multi Document Interface) tab system. You can open multiple schematic sheets or libraries at the same time.

* **Switch tabs:** Click a tab title at the top of the canvas to switch between open files.
* **Close tabs:** Click the `X` on the tab, or use `Ctrl + W`.

:::warning[Note]
Detaching tabs into separate windows via drag-and-drop is not supported yet. Use the tab bar to navigate.
:::

<video controls width="100%">
  <source src="/videos/MDI_SW.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>

---

## 4. Keymap settings

To speed up your workflow, WireFrame lets you customize all hotkeys to match your habits (or to mimic Altium/KiCad-style shortcuts).

**How to open it:**
1.  Go to **Edits** → **Keymap**.
2.  Search for the command you want.
3.  Press the new key combination to bind.

![Key_map](/img/Keymap.png)

---

## 5. Helper tools

For accurate and professional schematics, make sure to use these helper tools:

### Grid & Snap
The grid helps align components and wires.
* **Toggle Grid:** Show/hide the grid.
* **Grid Size:** Change the grid spacing (e.g., 2.54mm, 1.27mm).

### Crosshair
Helps align objects over longer distances.

### Title block
Each sheet includes a standard title block. Fill in engineering metadata here for documentation outputs.
* *Engineer Name*
* *Revision*
* *Date*

<video controls width="100%">
  <source src="/videos/Page_Setup.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>

---

## Toolbar quick reference

Below are the most commonly used toolbar icons:

| Icon | Tool | Shortcut (default) | Purpose |
| :---: | :--- | :---: | :--- |
| 🖱️ | **Select** | `S` | Select objects (single/box selection). |
| ✏️ | **Wire** | `W` | Draw electrical connections (wires). |
| 🔌 | **Component** | `C` | Place components from the library. |
| 🎨 | **Graphics** | `G` | Draw annotations (Line, Rect, Circle). |

:::tip[Tip]
Keep your left hand on the keyboard for quick tool switching, and your right hand on the mouse for drawing.
:::