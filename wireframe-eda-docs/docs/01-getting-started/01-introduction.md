---
sidebar_position: 2
id: installation
title: Installation
description: Step-by-step guide to install WireFrame EDA on macOS and Ubuntu Linux.
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import Admonition from '@theme/Admonition';

# Installation Guide

**WireFrame EDA** is designed to be lightweight and efficient. Choose your operating system below to get started.

---

## Download Latest Version

Get the latest stable release directly from our GitHub repository.

<div style={{display: 'flex', gap: '10px', marginBottom: '20px'}}>
  <a className="button button--primary button--lg" href="https://github.com/CaSauCoin/WireFrame_Product/tags" target="_blank">
    Download Installers
  </a>
  <a className="button button--secondary button--lg" href="https://github.com/CaSauCoin/WireFrame_Product/tags" target="_blank">
    View All Versions
  </a>
</div>

---

## Setup Instructions

<Tabs
  defaultValue="linux"
  values={[
    {label: 'Linux (Ubuntu/Debian)', value: 'linux'},
    {label: 'macOS', value: 'mac'},
  ]}>

  <TabItem value="linux">
    <Admonition type="info" title="Compatibility">
      Tested on **Ubuntu 20.04 LTS**, **22.04 LTS**, **Debian 11+**, and **Linux Mint**.
    </Admonition>

    ### Step 1: Download
    Download the latest `.deb` package from the link above.

    ### Step 2: Install via Terminal
    Navigate to your download folder and run:

    ```bash
    # Replace x.x.x with the version you downloaded
    sudo dpkg -i wireframe-x.x.x-Linux.deb
    ```

    ### Step 3: Troubleshooting
    If you see dependency errors, run this magic command to fix them:

    ```bash
    sudo apt-get install -f
    ```

    **Done!** Type `wireframe` in your terminal to launch.
  </TabItem>

  <TabItem value="mac">
    ### Step 1: Download & Mount
    Download the `.dmg` file and double-click to open it.

    ### Step 2: Drag & Drop
    Drag the **WireFrame** icon into the **Applications** folder provided in the window.
    Run Cmd: sudo xattr -cr /Applications/WireFrame.app

    ### Step 3: First Launch (Important!)
    1. Go to **Applications** folder.
    2. **Right-click** the WireFrame app.
    3. Select **Open**.
    4. Click **Open** again in the warning dialog.
    
    *You only need to do this once.*
  </TabItem>

</Tabs>

---

## 💻 System Requirements

Minimum specs to ensure 3D rendering runs smoothly.

| Component | Minimum | Recommended |
| :-- | :-- | :-- |
| **OS** | Ubuntu 20.04 / macOS 11 | Ubuntu 22.04 / macOS 13+ |
| **CPU** | Dual Core | Quad Core (for Auto-routing) |
| **RAM** | 4 GB | 8 GB |
| **Graphics** | Integrated Graphics | Dedicated GPU (NVIDIA/AMD) |