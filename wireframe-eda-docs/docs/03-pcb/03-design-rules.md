---
sidebar_position: 4
title: Design Rules & DRC
description: Guide on setting up design rules and performing group-based DRC checks.
---

import useBaseUrl from '@docusaurus/useBaseUrl';

# Design Rules & DRC Management

This feature allows you to define physical constraints (trace width, safety clearance) for specific net groups and perform Design Rule Checks (DRC) to ensure board integrity.

## 1. Creating Net Groups

Before setting up specific rules, you need to organize related signals (e.g., Power, GND, High-Speed) into groups.

1. Open the **Net Manager** panel from the left toolbar.
2. Select the nets you want to group (hold `Ctrl` or `Shift` to select multiple nets).
3. Right-click and choose **Create Net Group**.
4. Assign a name to the group (e.g., `PWR_5V`, `DATA_BUS`).

<div style={{textAlign: 'center', margin: '20px 0'}}>
  <img 
    src={useBaseUrl('/img/docs/net-manager-group.png')} 
    alt="Net Group Creation Interface in WireFrame EDA" 
    style={{maxWidth: '100%', border: '1px solid #ddd', borderRadius: '4px'}}
  />
  <p><i>Figure 1: Creating groups in Net Manager</i></p>
</div>

## 2. Configuring Design Rules

Once net groups are established, you can apply specific technical parameters to them.

1. Navigate to **Design** > **Design Rules**.
2. In the Rules Editor window, switch to the **Net Group Rules** tab.
3. Select your newly created group from the list.
4. Configure the parameters:
   * **Trace Width:** Min, Max, and Preferred width.
   * **Clearance:** Minimum safety distance to other pads or tracks.
   * **Via Style:** Default via dimensions for this group.

<div style={{textAlign: 'center', margin: '20px 0'}}>
  <img 
    src={useBaseUrl('/img/docs/rule-editor.png')} 
    alt="Design Rules Editor Window" 
    style={{maxWidth: '100%', border: '1px solid #ddd', borderRadius: '4px'}}
  />
</div>

## 3. Running Group-based DRC

To save time during the routing process, you can verify DRC on critical groups specifically, rather than scanning the entire board.

1. Click the **DRC Check** icon on the toolbar (or press `F7`).
2. In the DRC dialog, under the **Scope** section, select **Specific Net Groups**.
3. Check the boxes for the groups you wish to inspect (e.g., only check `High_Voltage`).
4. Click **Run DRC**.

Violations will be listed in the bottom panel. You can double-click on an error to zoom in to the exact location on the PCB.

<div style={{textAlign: 'center', margin: '20px 0'}}>
  <img 
    src={useBaseUrl('/img/docs/drc-result.png')} 
    alt="DRC Check Results" 
    style={{maxWidth: '100%', border: '1px solid #ddd', borderRadius: '4px'}}
  />
</div>

:::tip Pro Tip
Enable **Live DRC** in your preferences to visualize errors in real-time while routing critical net groups.
:::