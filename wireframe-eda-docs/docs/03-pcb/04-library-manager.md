---
sidebar_position: 4
title: Library Manager
description: Configure library paths, manage tables, and organize global vs. project assets.
---

import useBaseUrl from '@docusaurus/useBaseUrl';


# Library Manager

The **Library Manager** is the control center for all your component assets. It allows you to map local file paths to WireFrame's internal library tables, ensuring your projects are portable and organized.

To access the Library Manager, go to **Preferences > Manage Symbol/Footprint Libraries**.

## 1. Global vs. Project Libraries

WireFrame uses a two-tier system for managing libraries:

### Global Libraries
* **Scope:** Available to **all projects** on your computer.
* **Use Case:** Standard components (Resistors, Capacitors, Common MCUs).
* **Location:** Typically stored in your systeam's documents folder or a shared network drive.

### Project Specific Libraries
* **Scope:** Only available to the **current active project**.
* **Use Case:** Custom components specific to a single design, or experimental parts.
* **Portable:** When you share your project folder, these library links travel with it (if using relative paths).

<!-- ![Library Manager Dialog](/img/docs/library-manager-dialog.png) -->

## 2. Adding a New Library

You can add existing KiCad (`.kicad_sym`, `.pretty`) or WireFrame libraries easily.

1.  **Open Library Manager.**
2.  Click the **Add Library (Folder Icon)** button.
3.  Navigate to your `.kicad_sym` file (for symbols) or `.pretty` folder (for footprints).
4.  **Nickname:** Give the library a short, recognizable nickname (e.g., `My_Sensors`). This nickname is what you will type in the search bar.

:::tip Legacy Support
WireFrame also supports legacy `.lib` files. However, we recommend converting them to `.kicad_sym` format for better performance and feature support.
:::

<video controls width="100%">
  <source src={useBaseUrl('/videos/Create_FP.mp4')} type="video/mp4" />
  Your browser does not support the video tag.
</video>

## 3. Managing Library Tables

The library list is essentially a mapping table.

* **Active:** Uncheck this box to hide a library from the editor without deleting the link. This speeds up search performance if you have massive libraries loaded.
* **Visible:** Controls whether the library appears in the side panel by default.
* **Path Variables:** You can use environment variables (like `${KICAD6_SYMBOL_DIR}` or `${WIRE_USER_LIB}`) in the path field. This is crucial for teams sharing libraries across different computers.

<video controls width="100%">
  <source src={useBaseUrl('/videos/Load_Footprint.mp4')} type="video/mp4" />
  Your browser does not support the video tag.
</video>

## 4. Troubleshooting

### Library Not Found
If a library row is highlighted in **Red**, the file path is invalid.
* Check if the file was moved or deleted.
* If using Path Variables, ensure the environment variable is set correctly in **Preferences > Configure Paths**.

### Duplicate Nicknames
Every library must have a unique nickname. If you import two libraries named "Connectors", WireFrame will ask you to rename the second one (e.g., "Connectors_v2").