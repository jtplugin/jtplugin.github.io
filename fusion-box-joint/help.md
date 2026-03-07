# JT Box Joint — User Guide

**Version:** 1.0.0  
**Compatible with:** Autodesk® Fusion® 2.0.18000 or later  
**Developer:** Giovanni Tommasi — JT Plugin Development

---

## 📋 Overview

JT Box Joint is an Autodesk® Fusion® add-in that generates fully parametric finger-joint boxes ready for laser cutting — directly inside your design, with no external tools required.

Starting from any rectangular solid, the add-in automatically calculates all panels, applies interlocking tabs on every edge, compensates for laser kerf, and optionally lays all parts flat on the XY plane for immediate DXF export.

![Plugin dialog with face selected](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/UISelectedFace.png)

---

## 🚀 Quick Start

### Step 1 — Open the dialog
1. Open your Fusion design (or create a rectangular solid)
2. Switch to the **Solid** workspace
3. In the **Create** panel, click **JT Box Joint**

![JT Box Joint in the Create menu](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/CommandMenu.png)

### Step 2 — Select the Open Face
Click the **Open Face** field, then select the planar face that will be the opening of your box — typically the top face. The add-in derives the box's long (L) and short (S) dimensions from the opposite (bottom) face automatically.

### Step 3 — Set the parameters
Enter **Thickness** (material thickness) and **Tab Width**, then configure any additional options described below.

### Step 4 — Click OK
All panels are generated and assembled in the 3D view with correctly interlocking finger joints on every edge.

![Resulting box without dividers](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/ResultNoDivs.png)

---

## 🔧 Parameters

### Open Face
The planar face that defines the box opening. Long (L) and short (S) edge dimensions are derived automatically from the bottom face. Select it directly from the 3D view while the dialog is open.

### Thickness
Material thickness in current document units. This value controls the depth of every tab and slot across all panels.

### Tab Width *(Pro)*
Width of each finger/tab. In **Trial**, this is fixed at 3× the material thickness. In **Pro**, any value can be entered freely.

### Aesthetic Tabs *(Pro)*
When enabled, the number of tabs per edge is adjusted so that all tabs have equal width and the layout is visually balanced. When disabled, tabs have exactly the requested width and the last tab on each edge may be partial.

### Divisions along longer edge / shorter edge *(Pro)*
Number of internal dividers along each axis. Set to **1** for no dividers. Each value above 1 adds one divider, which interlocks correctly with all surrounding panels via matching slots.

![Box with internal dividers](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/ResultWDivs.png)

*Example: 3 divisions along longer edge × 2 along shorter edge*

![Divider interlocking detail](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/DivDetails.png)

### Create New Component
When enabled, all generated panels are placed in a new component under the root. This keeps the original geometry untouched and makes the output easier to manage.

---

## 🏭 Flat Layout *(Pro)*

The Flat Layout section generates a flat copy of all panels arranged on the XY plane — ready for DXF/DWG export and laser cutting.

![Flat layout panel disposition](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/Flat%20Layout%20disposition.png)

### Create Flat Layout
Enable to generate the flat layout. All panels are unfolded and placed sequentially on the XY plane.

![Flat layout sketch](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/FlatLayoutSketch.png)

### Kerf
Laser kerf compensation offset in current document units. All tab and slot dimensions are adjusted by this value automatically. Set to **0** for no compensation.

### Keep Original Panels
When enabled, the 3D assembled body is retained alongside the flat layout. When disabled, only the flat layout is kept — useful when you only need the cut files.

---

## ⚙️ Advanced *(Pro)*

### Wrap in Custom Feature
Groups the entire box joint operation — all cuts, extrusions, and copies — into a single **Custom Feature** entry in the Fusion timeline.

![Custom Feature in timeline](https://raw.githubusercontent.com/jtplugin/fusion-box-joint/main/screenshots/TimelineCustomFeature.png)

**To edit after creation:** double-click the *JT Box Joint* feature in the timeline. The dialog reopens with all original values, ready to modify.

> **Note:** Wrap in Custom Feature and Flat Layout Subcomponent cannot be active at the same time.

### Flat Layout Subcomponent
Places the flat layout panels in a dedicated sub-component for cleaner browser and timeline organisation. Available when **Wrap in Custom Feature** is disabled.

---

## 🔄 Editing an Existing Box

If the box was created with **Wrap in Custom Feature** enabled, double-click the *JT Box Joint* entry in the timeline to reopen the dialog and change any parameter. The model updates automatically.

If Custom Feature was not used, parameters cannot be changed after creation — undo and recreate if needed.

---

## 🆚 Trial vs Pro

| Feature | Trial | Pro |
|---------|:-----:|:---:|
| Open Face, Thickness, Create New Component | ✅ | ✅ |
| Tab Width (custom) | — ¹ | ✅ |
| Aesthetic Tabs | — | ✅ |
| Divisions (longer / shorter edge) | — | ✅ |
| Flat Layout, Kerf, Keep Original Panels | — | ✅ |
| Wrap in Custom Feature | — | ✅ |
| Flat Layout Subcomponent | — | ✅ |

¹ In Trial, Tab Width is fixed at 3× the material thickness.

Pro licenses are available on the [Autodesk App Store](https://apps.autodesk.com). After purchase, restart Fusion to activate your licence. If the licence is not detected, use **Refresh Entitlement** from the add-in menu.

Full feature details: [features.md](features.md)

---

## 🛠️ Troubleshooting

**The dialog opens but OK does nothing**  
Check that the Open Face field shows a valid selection (highlighted in blue). The face must be a flat, rectangular planar face.

**Tabs look uneven**  
Enable **Aesthetic Tabs** (Pro) to automatically balance tab count per edge.

**Flat layout panels overlap**  
This may occur with very small tab widths relative to panel size. Increase Tab Width or enable Aesthetic Tabs.

**Custom Feature edit dialog does not open**  
Make sure you are double-clicking the *JT Box Joint* feature in the timeline, not a sub-feature inside it. Collapse the group first if expanded.

**Licence not detected after purchase**  
Restart Fusion. If still not detected, use **Refresh Entitlement** from the add-in menu to force a new licence check.

---

## 📞 Support

- **Email:** [jtplugin@ajl.vision](mailto:jtplugin@ajl.vision)
- **GitHub Issues:** [github.com/jtplugin/fusion-box-joint/issues](https://github.com/jtplugin/fusion-box-joint/issues)
- **Response time:** 24–48 hours (Pro users priority)

---

## 📜 Legal

**Copyright © 2025 Giovanni Tommasi — JT Plugin Development**

This software is distributed through the Autodesk App Store under the terms specified in our Terms of Service. By using this plugin you agree to our Privacy Policy and Terms of Service.

- [Privacy Policy](https://jtplugin.github.io/privacy-policy)
- [Terms of Service](https://jtplugin.github.io/terms)

---

*This documentation covers version 1.0.0 of JT Box Joint. For the latest updates, check the [Autodesk App Store](#) or the [GitHub repository](https://github.com/jtplugin/fusion-box-joint).*
