---
sidebar_position: 3
title: Libraries & Components
description: Manage component libraries, leverage the KiCad ecosystem, and automate symbol creation.
---

import useBaseUrl from '@docusaurus/useBaseUrl';

# Libraries & Components

WireFrame EDA is built on a core philosophy: **Don't reinvent the wheel.** Our library system is designed to let you instantly tap into millions of existing components from the open-source ecosystem while providing powerful tools to generate custom parts in seconds.

## 1. Native KiCad Integration

Why start from scratch? WireFrame supports **Direct Import** of standard KiCad libraries, allowing you to leverage the vast community-driven database immediately.

* **Format Support:** Seamlessly import `.kicad_sym` (Symbol Library) and `.kicad_mod` files.
* **Seamless Rendering:** The WireFrame engine natively parses and renders geometries, pins, and field information exactly as they appear in the original software.

:::tip Access Infinite Components
You can download standard libraries from the [SnapMagic](https://www.snapeda.com/home/) or third-party repositories like SnapEDA or UltraLibrarian and load them directly into WireFrame.
:::

<video controls width="100%">
  <source src={useBaseUrl('/videos/Library.mp4')} type="video/mp4" />
  Your browser does not support the video tag.
</video>

## 2. Smart Symbol Generator

For ICs or components that don't have an existing library, the built-in **Lib Gen** tool allows you to create schematic symbols in just a few clicks, eliminating tedious manual drawing.

**The Automated Workflow:**
1.  **Pin Definition:** Input the pin count or paste a pin list directly from a datasheet.
2.  **Package Selection:** Choose the package style (Dual-Inline, Quad-Flat, Matrix, etc.).
3.  **Generate:** WireFrame automatically calculates the body dimensions and arranges the pins optimally.

<!-- ![Smart Symbol Generator Interface](/img/docs/symbol-generator-ui.png) -->

## 3. Dynamic Attributes System

WireFrame replaces rigid static text with a flexible **Dynamic Attributes** system. This ensures that symbol data is always synchronized with the component properties.

* **Text-to-Attribute:** Automatically converts placeholder text (e.g., `>NAME`, `>VALUE`) into functional, editable attributes.
* **Global Sync:** Modifying a component's value in the Properties panel instantly updates all related text on the schematic canvas.

<video controls autoPlay loop muted width="100%">
  <source src="/img/docs/dynamic-attributes.mp4" type="video/mp4"/>
</video>

## 4. Centralized Library Manager

Keep your workspace organized and efficient with the **Library Manager**.

* **Toggle Control:** Enable or disable specific libraries to keep your search results clean and relevant.
* **Categorization:** Libraries are organized by logic groups (MCU, Power, Connectors, etc.).
* **Fast Search:** Locate components instantly by name, description, or tags.

<!-- ![Library Manager Overview](/img/docs/library-manager.png) -->