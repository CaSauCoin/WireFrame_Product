---
sidebar_position: 3
title: Libraries & Components
description: Importing libraries, creating symbols, and managing attributes.
---

# Libraries & Components

WireFrame offers a flexible library system that allows you to reuse existing assets and create new ones quickly.

## KiCad Compatibility
Don't start from scratch. WireFrame allows you to "recycle" and import standard **KiCad libraries**.
* Import `.lib` or `.kicad_sym` files directly.
* Geometries and pins are automatically converted to WireFrame native formats.

## Symbol Generator
The built-in **Lib Gen** tool helps you create schematic symbols for new ICs rapidly:
1. Define the number of pins.
2. Set the package style (DIP, QFP, etc.).
3. Generate the symbol body and pin assignments automatically.

## Attributes System
WireFrame uses a dynamic attribute system for component text:
* **Dynamic Conversion:** Convert static text (like "PinName" or "ComponentName") into functional attributes.
* **Property Editing:** Attributes are linked to the component properties, allowing for global updates.

## Library Manager
Organize your imported and custom libraries in the centralized Library Manager. You can enable or disable specific library sets to keep your search results clean.
