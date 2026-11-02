<!-- GENERATED FROM .appstore/metadata.json; DO NOT EDIT BY HAND -->

# JT Flat Layout Help — v1.3.0

**Developer**: Giovanni Tommasi · **Support**: [jtplugin@ajl.vision](mailto:jtplugin@ajl.vision)

---

## 📋 Overview

Unroll an Autodesk® Fusion® component into a flat, laser-ready layout in one click. Free trial: up to 5 panels, DXF export. Upgrade for kerf compensation and SVG.

---

## 🚀 Quick Start

1. Open the Design workspace in Autodesk® Fusion® and click **JT Flat Layout** in the JTPLUGIN panel.
2. Select the component whose bodies you want to lay flat.
3. Set the gap between panels and, in Pro, the laser kerf compensation.
4. Click **OK**: every body is unrolled onto the XY plane as a flat panel, ready for DXF/SVG export.

---

## 📐 Parameters

- **Target Component**: The component (or root) whose solid bodies are arranged flat on the XY plane.
- **Kerf** *(Pro only)*: Laser kerf compensation: flat profiles are offset outward by this amount. Fixed at 0 in Trial.
- **Gap Between Panels**: Horizontal spacing between the flat panels in the layout.
- **Keep Original Bodies**: Keep the 3D bodies alongside the flat layout, or leave only the layout.
- **Flat Layout in Sub-Component**: Create the layout inside a new "Flat Layout" sub-component.
- **Show Body Names / Name Text Height**: Label each panel in the layout sketch with its body name, at the chosen text height.
- **Export as DXF**: After OK, a Save dialog exports the flat layout sketch as DXF (native Fusion export, all tiers).
- **Export as SVG** *(Pro only)*: Multi-layer SVG: blue = outer cut, red = kerf/inner, black = labels. LightBurn-ready.
- **Delete layout after export**: Remove the layout from the model once the file is saved. Useful when only the file is needed.
- **Wrap in Custom Feature** *(Pro only)*: Group the operations as an editable Custom Feature in the timeline, so parameters can be changed later.

---

## 🆓 Trial vs Pro

| Feature | Pro | Trial |
|---------|---|---|
| Kerf compensation | ✅ | Fixed at 0 |
| SVG export | ✅ | Not available |
| Custom Feature wrap | ✅ | One-shot, not editable |
| Max panels per layout | Unlimited | 5 |

---

## 🛠️ Troubleshooting

**Nothing visible happens after OK**

With a single body the flat panel overlaps the model. Switch to the top view or disable Keep Original Bodies. The command works on the bodies of the selected component: select a multi-body component.

**Trial: "maximum panels" message**

The Trial version lays out up to 5 bodies per layout. Split the component or upgrade to JT Flat Layout.

**Kerf or SVG export are greyed out**

These are Pro features. In Trial the kerf is fixed at 0 and only DXF export is available.

**Layout is not editable from the timeline**

Enable Wrap in Custom Feature (Advanced group, Pro) before generating. Trial layouts are one-shot.

---

## 📞 Support

- 📧 Email: [jtplugin@ajl.vision](mailto:jtplugin@ajl.vision)
- 🌐 Help: [https://jtplugin.github.io/fusion-flat-layout/help](https://jtplugin.github.io/fusion-flat-layout/help)
- 🐛 Issues: [github.com/jtplugin/jtplugin.github.io/issues](https://github.com/jtplugin/jtplugin.github.io/issues)

---

## 📜 Legal

Copyright 2026 Giovanni Tommasi — JT Plugin Development.
All rights reserved. Licensed via Autodesk App Store.

- [Privacy Policy](https://jtplugin.github.io/privacy-policy)
- [Terms of Service](https://jtplugin.github.io/terms)
