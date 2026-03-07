# JT 3D Slicer - User Guide

**Version:** 1.0.0  
**Compatible with:** Autodesk® Fusion®  
**Developer:** Giovanni Tommasi - JT Plugin Development

---

## 📋 Overview

JT 3D Slicer is a powerful plugin for Autodesk® Fusion® that enables you to slice 3D bodies into multiple parts along specified axes. Perfect for laser cutting, CNC machining, 3D printing preparation, and manufacturing workflows where you need to split objects into manageable pieces.

The plugin is available in two versions:
- **Trial Version:** Basic slicing with limitations
- **Pro Version:** Full-featured slicing with advanced capabilities

---

## 🚀 Quick Start Guide

### Step 1: Access the Plugin
1. Open Fusion
2. Navigate to the **SOLID** workspace
3. In the **CREATE** panel, locate the **JT 3D Slicer** button
4. Click the button to launch the slicing dialog

### Step 2: Select Your 3D Body
1. In the dialog, click the **Body Selection** field
2. Select the 3D body you want to slice from your design
3. The plugin will automatically analyze the body dimensions

### Step 3: Configure Slicing Parameters
1. **Slice Thickness:** Enter the desired thickness for each slice (in current units)
2. **Slice Axis:** Choose the direction for slicing:
   - **Z-axis:** Horizontal slices (Trial & Pro)
   - **X-axis:** Vertical slices along width (Pro only)
   - **Y-axis:** Vertical slices along depth (Pro only)
3. **Name Prefix:** Customize the naming pattern for sliced parts (Pro only)

### Step 4: Execute Slicing
1. Review the slice count preview
2. Click **OK** to execute the slicing operation
3. The plugin will create individual bodies for each slice
4. Pro version automatically organizes slices in timeline groups

---

## 🆓 Trial Version Features

The trial version provides essential slicing capabilities:

### ✅ Included Features:
- **Basic Slicing:** Up to 10 slices per operation
- **Z-Axis Only:** Horizontal slicing direction
- **Automatic Naming:** Standard naming convention
- **Body Analysis:** Dimension validation and warnings

### ⚠️ Limitations:
- Maximum 10 slices per operation
- Z-axis slicing only
- No timeline grouping
- No custom naming options
- No X/Y axis slicing

### 💡 Trial Version Workflow:
1. Select body to slice
2. Set slice thickness (minimum 0.1mm)
3. Plugin automatically calculates slice count
4. If more than 10 slices needed, reduces to 10 with notification
5. Creates sliced bodies with standard names

---

## 🚀 Pro Version Features

The Pro version unlocks the full potential of 3D slicing:

### ✅ Advanced Features:
- **Unlimited Slicing:** No limit on slice count
- **Multi-Axis Support:** X, Y, and Z-axis slicing
- **Timeline Grouping:** Organizes slices in timeline folders
- **Custom Naming:** Personalized naming patterns
- **Priority Support:** Direct email support

### 🎯 Pro Version Workflow:
1. Select body to slice
2. Choose any axis direction (X, Y, or Z)
3. Set custom thickness and naming
4. Execute unlimited slicing operations
5. Automatic timeline organization
6. Professional naming conventions

---

## 📐 Detailed Usage Instructions

### Body Selection
- **Supported Types:** Solid bodies, surface bodies
- **Requirements:** Body must be a single, continuous object
- **Size Limits:** Maximum 100cm in any dimension
- **Validation:** Plugin checks for valid geometry automatically

### Slice Thickness Configuration
- **Minimum Thickness:** 0.01cm (0.1mm)
- **Maximum Thickness:** 10cm
- **Units:** Uses current Fusion document units
- **Smart Calculation:** Plugin calculates optimal slice count
- **Warnings:** Alerts for very thin slices or excessive slice counts

### Axis Selection (Pro)
- **Z-Axis (Horizontal):** Slices parallel to XY plane
- **X-Axis (Vertical):** Slices parallel to YZ plane  
- **Y-Axis (Vertical):** Slices parallel to XZ plane
- **Visual Preview:** Shows slice direction in dialog
- **Automatic Orientation:** Respects current component orientation

### Naming Conventions
**Trial Version:**
- Format: `[BodyName]_Slice_01`, `[BodyName]_Slice_02`, etc.
- Automatic numbering with zero-padding
- No customization options

**Pro Version:**
- **Custom Prefix:** Choose your own naming pattern
- **Smart Numbering:** Automatic sequential numbering
- **Pattern Examples:**
  - `LaserCut_Part_01`, `LaserCut_Part_02`
  - `Section_A_01`, `Section_A_02`
  - `Custom_Name_001`, `Custom_Name_002`

---

## 🔧 Advanced Features (Pro Only)

### Timeline Organization
The Pro version automatically creates organized timeline groups:
- **Group Name:** Based on original body name
- **Chronological Order:** Slices organized sequentially
- **Easy Management:** Expand/collapse groups for clean timeline
- **Batch Operations:** Apply changes to entire slice groups

### Multi-Axis Slicing Strategies

**Z-Axis (Horizontal) - Best For:**
- Laser cutting applications
- Layer-based manufacturing
- Flat sheet material preparation
- Traditional horizontal slicing

**X-Axis (Vertical Width) - Best For:**
- Side-view cross-sections
- Profile cutting
- Width-based segmentation
- Architectural sections

**Y-Axis (Vertical Depth) - Best For:**
- Front/back sectioning
- Depth-based analysis
- Longitudinal cuts
- Engineering cross-sections

### Thickness Optimization Tips
- **Laser Cutting:** Match material thickness (3mm, 6mm, etc.)
- **3D Printing:** Consider layer height multiples
- **CNC Machining:** Account for tool access and material waste
- **Assembly:** Plan for joining methods and tolerances

---

## ⚙️ Technical Specifications

### System Requirements
- **Software:** Autodesk Fusion (Version 2.0.18000 or later)
- **Operating System:** Windows 10/11, macOS 10.15+
- **Memory:** Minimum 8GB RAM recommended
- **Storage:** 50MB trial space for plugin files

### Performance Guidelines
- **Optimal Slice Count:** 5-50 slices for best performance
- **Large Bodies:** Bodies over 50cm may require longer processing
- **Complex Geometry:** Curved surfaces may increase processing time
- **Memory Usage:** Large slice counts consume more system memory

### File Format Support
- **Input:** Native Fusion bodies (solid and surface)
- **Output:** Individual Fusion bodies in current document
- **Export:** Compatible with all Fusion export formats
- **Integration:** Works with existing Fusion workflows

---

## 🛠️ Troubleshooting

### Common Issues and Solutions

**"Body selection is invalid"**
- Ensure you've selected a valid solid or surface body
- Check that body is not part of a component assembly
- Verify body has proper closed geometry

**"Slice thickness too small"**
- Minimum thickness is 0.01cm (0.1mm)
- Increase thickness value
- Check document units and scale

**"Too many slices calculated"**
- Trial version: Reduce thickness or upgrade to Pro
- Pro version: Confirm intention for large slice count
- Consider body size vs. thickness ratio

**"Slicing operation failed"**
- Check body geometry for errors
- Ensure adequate system memory
- Try simpler geometry or fewer slices

**F1 Help not working**
- Ensure internet connection is active
- Check firewall settings for browser access
- Try refreshing the help page

### Performance Optimization
- **Close unnecessary applications** before large slicing operations
- **Save your work** before running complex slicing
- **Use Preview mode** to verify settings before execution
- **Consider batch processing** for multiple bodies

---

## 📞 Support and Contact

### Trial Version Support
- **Documentation:** This help page and GitHub repository
- **Community:** GitHub Issues and discussions
- **Updates:** Automatic through Autodesk App Store

### Pro Version Support
- **Priority Email:** jtplugin@ajl.vision
- **Response Time:** 24-48 hours typical
- **Direct Assistance:** Personalized troubleshooting
- **Feature Requests:** Priority consideration for new features

### Additional Resources
- **GitHub Repository:** https://github.com/jtplugin/fusion-3d-slicer
- **Privacy Policy:** https://jtplugin.github.io/privacy-policy
- **Terms of Service:** https://jtplugin.github.io/fusion-3d-slicer/terms_of_service
- **Company Website:** https://github.com/jtplugin

---

## 🔄 Version History

### Version 1.0.0 (Current)
- Initial release with Trial and Pro versions
- Multi-axis slicing support (Pro)
- Timeline organization (Pro)
- Custom naming patterns (Pro)
- Comprehensive validation system
- F1 Help integration

### Planned Features
- Batch slicing for multiple bodies
- Advanced slicing patterns
- Export presets for common workflows
- Enhanced timeline management
- Performance improvements

---

## 📜 Legal Information

**Copyright © 2025 Giovanni Tommasi - JT Plugin Development**

This software is distributed through the Autodesk App Store under the terms specified in our Terms of Service. By using this plugin, you agree to our Privacy Policy and Terms of Service.

**Privacy:** We respect your privacy. This plugin does not collect or transmit your design data. License verification only transmits machine ID and license key information.

**Support:** For technical support, licensing questions, or feature requests, contact us at jtplugin@ajl.vision

---

*This documentation covers version 1.0.0 of JT 3D Slicer. For the latest updates and features, please check the Autodesk App Store or our GitHub repository.*
