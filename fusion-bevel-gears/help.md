<!-- GENERATED FROM .appstore/metadata.json; DO NOT EDIT BY HAND -->

# JT Bevel Gears Help — v1.0.0

**Developer**: Giovanni Tommasi · **Support**: [jtplugin@ajl.vision](mailto:jtplugin@ajl.vision)

---

## 🚀 Quick Start

1. Open the Solid workspace in Autodesk® Fusion® and click **JT Bevel Gears** in the Create panel.
2. Configure tooth geometry (z, m, δ, α, b) in the left panel — derived values and SVG preview update live.
3. Select a positioning mode and placement point in the Fusion dialog.
4. Click **OK** to generate the bevel gear solid body.

---

## 📐 Parameters

- **Number of Teeth (z)**: Number of gear teeth. Trial: restricted to a limited range.
- **Module (m)**: External module — controls tooth size and gear diameter.
- **Pitch Cone Angle (δ)**: Half-angle of the pitch cone. Trial: restricted to a subset of values.
- **Pressure Angle (α)**: Standard tooth profile angle.
- **Face Width (b)**: Width of the gear tooth along the pitch cone.
- **Base Center positioning**: Place the gear centered on a construction or sketch point, axis along component Z.
- **Apex positioning** *(LT+)*: Position the gear from the cone vertex with a reference plane.
- **Automatic Rotation Axes** *(LT+)*: Generates rotation axes automatically after each gear creation.
- **Gear Naming** *(LT+)*: Set a custom name for the generated gear from the UI.
- **Feature Grouping** *(LT+)*: Groups generated features in the Fusion timeline for a clean, editable history.
- **Bevel Gear Mate** *(Pro only)*: Generate a mating R2 gear from an existing R1 — reads R1 geometry and places R2 in correct mesh position.

---

## 🆓 Trial vs Pro

| Feature | Pro | LT | Trial |
|---------|---|---|---|
| Commands | {'main': True, 'mate': True, 'link': False} | {'main': True, 'mate': False, 'link': False} | {'main': True, 'mate': False, 'link': False} |
| Auto axes | ✅ | ✅ | ❌ |
| Rotation refs | ✅ | ❌ | ❌ |
| Apex placement allowed | ✅ | ✅ | ❌ |
| Gear naming | ✅ | ✅ | ❌ |
| Feature grouping | ✅ | ✅ | ❌ |
| Max generations per session | — | — | 3 |
| Limited angles | — | — | True |
| Limited tooth counts | — | — | True |

---

## 🛠️ Troubleshooting

**Generation fails with a geometry error**

Check that module (m) and face width (b) are within valid range for the chosen tooth count and cone angle. Very small modules with many teeth can exceed Fusion geometry limits.

**SVG preview not updating**

Click into another parameter field to trigger recalculation. If the issue persists, close and reopen the palette.

**Trial session limit reached (3 gears)**

The Trial version allows up to 3 gear generations per Fusion session. Restart Fusion to reset the counter, or upgrade to LT/Pro for unlimited generations.

**Gear placed at wrong position**

Verify the selected placement point is a valid construction point. In Base Center mode the gear axis follows the active component Z direction.

---

## 📞 Support

- 📧 Email: [jtplugin@ajl.vision](mailto:jtplugin@ajl.vision)
- 🌐 Help: [https://jtplugin.github.io/fusion-bevel-gears/help](https://jtplugin.github.io/fusion-bevel-gears/help)
- 🐛 Issues: [github.com/jtplugin/jtplugin.github.io/issues](https://github.com/jtplugin/jtplugin.github.io/issues)

---

## 📜 Legal

Copyright 2026 Giovanni Tommasi — JT Plugin Development.
All rights reserved. Licensed via Autodesk App Store.

- [Privacy Policy](https://jtplugin.github.io/privacy-policy)
- [Terms of Service](https://jtplugin.github.io/terms)
