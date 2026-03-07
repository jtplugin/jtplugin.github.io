# JT Box Joint — Features

**Version:** 1.0.0  
**Compatible with:** Autodesk® Fusion® 2.0.18000 or later  
**Platform:** Windows 10/11, macOS 10.15+

---

## Trial vs Pro

| Feature | Trial | Pro |
|---------|:-----:|:---:|
| **Open Face selection** | ✅ | ✅ |
| **Thickness** | ✅ | ✅ |
| **Create New Component** | ✅ | ✅ |
| **Tab Width** (custom) | — ¹ | ✅ |
| **Aesthetic Tabs** | — | ✅ |
| **Divisions along longer edge** | — | ✅ |
| **Divisions along shorter edge** | — | ✅ |
| **Create Flat Layout** | — | ✅ |
| **Kerf compensation** | — | ✅ |
| **Keep Original Panels** | — | ✅ |
| **Wrap in Custom Feature** | — | ✅ |
| **Flat Layout Subcomponent** | — | ✅ |

¹ In Trial, Tab Width is fixed at 3× the material thickness.

---

## Feature Descriptions

**Open Face** — The planar face of the solid that defines the box opening (typically the top). Long (L) and short (S) edge dimensions are derived automatically from the opposite face.

**Thickness** — Material thickness in current document units. Used to calculate tab depth and slot width on all panels.

**Tab Width** — Width of each finger/tab. In Trial, this is fixed at 3× the material thickness. In Pro, any value can be entered.

**Aesthetic Tabs** — When enabled, the number of tabs per edge is adjusted to achieve a visually balanced result. When disabled, tabs have exactly the requested width and the last tab may be partial.

**Divisions along longer edge / shorter edge** — Number of internal dividers along each axis. Set to 1 for no dividers. Each divider interlocks correctly with all surrounding panels via matching slots.

**Create New Component** — When enabled, all generated panels are placed in a new component under the root, keeping the original geometry untouched.

**Create Flat Layout** — Generates a flat copy of all panels arranged on the XY plane, ready for DXF/DWG export and laser cutting.

**Kerf** — Laser kerf compensation offset. All tab and slot dimensions are adjusted by this value automatically. Set to 0 for no compensation.

**Keep Original Panels** — When enabled, the 3D assembled body is kept alongside the flat layout. When disabled, only the flat layout is retained.

**Wrap in Custom Feature** — Groups the entire box joint operation into a single Custom Feature entry in the Fusion timeline. Double-click the feature to reopen the dialog and change any parameter at any time.

**Flat Layout Subcomponent** — Places the flat layout panels in a dedicated sub-component for cleaner browser and timeline organisation. Available when Custom Feature is disabled.

---

## Upgrade to Pro

Pro licenses are available on the [Autodesk App Store](https://apps.autodesk.com).  
After purchase, restart Fusion to activate your licence.

> 💡 **Need more flat layout options?** JT Box Joint includes essential flat layout functionality. For advanced nesting, multi-body layouts, and custom arrangement options, check out the dedicated **JT Flat Layout** plugin.  
If the licence is not detected, use **Refresh Entitlement** from the add-in menu.

---

**[← Back to JT Box Joint](README.md)** · **[Terms of Service](https://jtplugin.github.io/terms)** · **[Privacy Policy](https://jtplugin.github.io/privacy-policy)**
