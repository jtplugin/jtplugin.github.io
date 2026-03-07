# JT Magic Revolve - User Guide

**Version:** 1.0.0  
**Compatible with:** Autodesk® Fusion®  
**Developer:** Giovanni Tommasi - JT Plugin Development

---

## 📋 Overview

JT Magic Revolve is a powerful plugin for Autodesk® Fusion® that enables you to create multiple copies of 3D bodies with controlled translation and rotation along separate axes. Perfect for creating complex patterns, spirals, and repetitive structures where you need to generate multiple instances of objects with precise positioning and rotation control.

The plugin provides full-featured revolving with advanced capabilities for creating unlimited patterns and structures.

---

## 🚀 Quick Start Guide

### Step 1: Access the Plugin
1. Open Fusion
2. Navigate to the **SOLID** workspace
3. In the **CREATE** panel, locate the **JT Magic Revolve** button
4. Click the button to launch the revolving dialog

### Step 2: Select Your 3D Body
1. In the dialog, click the **Body to Duplicate** field
2. Select the 3D body you want to revolve from your design
3. The plugin will automatically analyze the body properties

### Step 3: Configure Translation Axis
1. **Translation Axis:** Choose the axis for body movement (REQUIRED):
   - **Supported Types:** Linear edges, sketch lines, construction axes
   - **Purpose:** Defines the direction of body movement

### Step 4: Configure Rotation Axis (Optional)
1. **Rotation Axis:** Choose the axis for body rotation (OPTIONAL):
   - **Supported Types:** Linear edges, sketch lines, construction axes
   - **Purpose:** Defines the axis around which bodies rotate
   - If not selected, will use the translation axis

### Step 5: Set Operation Parameters
1. **Operation Priority:** Choose the order of operations:
   - **Rotation:** Rotate first, then translate (classic spirals)
   - **Translation:** Translate first, then rotate (distributed patterns)
2. **Translation Distance:** Enter the spacing between bodies (in current units)
3. **Number of Pieces:** Specify how many bodies to create (up to 1000)
4. **Rotation Angle:** Set the rotation increment between bodies
5. **Spacing Correction Angle (Optional):** Angle between translation axis and desired spacing direction
6. **Name Root:** Customize the naming pattern for created bodies
7. **Create New Component:** Option to create a new component for the revolved bodies

### Step 6: Execute Revolving
1. Review the preview of the operation
2. Click **OK** to execute the revolving
3. The plugin will create individual bodies with specified positioning and rotation
4. Bodies are automatically organized in timeline groups

---

## 🚀 Plugin Features

JT Magic Revolve provides comprehensive revolving capabilities:

### ✅ Core Features:
- **Unlimited Revolving:** Up to 1000 bodies per operation
- **All Axis Types:** Linear edges, sketch lines, construction axes
- **Timeline Grouping:** Organizes bodies in timeline folders
- **Custom Naming:** Personalized naming patterns
- **Priority Support:** Direct email support
- **Clean Workflow:** Streamlined operation without interruption

### 🎯 Workflow:
1. Select body to revolve
2. Choose translation axis (all types supported)
3. Optionally choose rotation axis (all types supported)
4. Set custom parameters and naming
5. Execute unlimited revolving operations
6. Automatic timeline organization
7. Professional naming conventions

---

## 📐 Detailed Usage Instructions

### Body Selection
- **Supported Types:** Solid bodies, surface bodies
- **Requirements:** Body must be a single, continuous object
- **Size Limits:** No specific size limitations
- **Validation:** Plugin checks for valid geometry automatically

### Translation Axis Configuration
- **Supported Types:** Linear edges, sketch lines, construction axes
- **Purpose:** Defines the direction of body movement
- **Visual Preview:** Shows axis direction in dialog

### Rotation Axis Configuration
- **Supported Types:** Linear edges, sketch lines, construction axes
- **Purpose:** Defines the axis around which bodies rotate
- **Optional:** If not selected, uses translation axis
- **Visual Preview:** Shows axis direction in dialog

### Operation Priority Configuration
- **Rotation→Translation:** Rotate first, then translate
  - Best for: Classic spiral patterns
  - Effect: Bodies rotate around their original position, then move
- **Translation→Rotation:** Translate first, then rotate
  - Best for: Distributed patterns
  - Effect: Bodies move to new position, then rotate around that position

### Distance Configuration
- **Positive Values:** Move in positive direction along axis
- **Negative Values:** Move in negative direction along axis
- **Zero Distance:** Bodies remain at same position (rotation only)
- **Units:** Uses current Fusion document units
- **Smart Calculation:** Plugin validates reasonable distances
- **Parametric Support:** Use expressions like "d1 * 2" or parameter names

### Number of Pieces Configuration
- **Maximum:** 1000 pieces per operation
- **Minimum:** 1 piece (original body only)
- **Validation:** Plugin warns for excessive body counts
- **Parametric Support:** Use expressions like "param + 1" or parameter names

### Rotation Angle Configuration
- **Positive Values:** Clockwise rotation
- **Negative Values:** Counter-clockwise rotation
- **Zero Angle:** No rotation between bodies
- **Range:** -360° to +360° per body
- **Cumulative:** Each body rotates relative to the previous
- **Parametric Support:** Use expressions like "angle_param + 15 deg" or parameter names

### Spacing Correction Angle Configuration
- **Purpose:** Compensates for the difference between translation axis direction and desired spacing direction
- **Problem Solved:** When objects need to be spaced in a different direction than the translation axis
- **Default:** 0° for no correction (standard behavior)
- **Formula:** corrected_distance = distance / cos(correction_angle)
- **Use Case:** Perfect for complex structures where objects must not intersect
- **Parametric Support:** Use parameters like "my_angle" or expressions like "atan(1/2)*180/pi"

**How Spacing Correction Works:**

**Scenario 1 - No Correction (0°):**
- Translation axis: Horizontal (X-axis)
- Desired spacing: Horizontal
- Result: Objects move horizontally with exact distance spacing

**Scenario 2 - With Correction (45°):**
- Translation axis: Diagonal (45° from horizontal)
- Desired spacing: Vertical (90° from horizontal)
- Correction angle: 45° (difference between diagonal and vertical)
- Result: Objects move diagonally but are spaced vertically

**Mathematical Explanation:**
- **Without correction:** Distance = 10mm along diagonal axis
- **With 45° correction:** Corrected distance = 10mm / cos(45°) = 14.14mm
- **Why:** The diagonal movement needs to be "stretched" to achieve the desired vertical spacing

**Real-World Examples:**
- **Spiral staircase:** Translation along spiral path, but steps need vertical spacing
- **Helical structures:** Translation along helix, but elements need radial spacing
- **Complex assemblies:** Translation along curved path, but components need linear spacing

**Practical Usage Guide:**

**Step 1 - Identify the Problem:**
- Your translation axis points in one direction (e.g., diagonal)
- But you want objects spaced in a different direction (e.g., vertical)
- Without correction, objects will be too close together

**Step 2 - Calculate Correction Angle:**
- Measure the angle between your translation axis and desired spacing direction
- Example: Translation axis = 30° from horizontal, Desired spacing = vertical (90°)
- Correction angle = 90° - 30° = 60°

**Step 3 - Apply the Correction:**
- Set "Spacing Correction Angle" to 60°
- The plugin automatically applies: corrected_distance = distance / cos(60°)
- Result: Objects move along 30° axis but are spaced vertically

**Step 4 - Verify Results:**
- Check that objects have the correct spacing in your desired direction
- Adjust correction angle if needed (small increments)
- Use parametric expressions for dynamic correction angles

### Component Management
- **Create New Component:** Option to create a new component for the revolved bodies
- **Performance Benefits:** Significantly improves performance with many bodies or iterations
- **Organization:** Keeps revolved bodies organized and separate from original geometry
- **Timeline Management:** Easier to manage and modify large numbers of bodies

**Performance Impact of New Component Creation:**

**Why New Components Improve Performance:**
- **Memory Management:** Fusion handles components more efficiently than loose bodies
- **Rendering Optimization:** Components are rendered as groups, reducing GPU load
- **Timeline Efficiency:** Operations on components are faster than individual bodies
- **Memory Footprint:** Lower memory usage for large numbers of bodies

**Performance Comparison:**

**Without New Component (Many Bodies):**
- Each body is processed individually
- Timeline becomes cluttered with hundreds of operations
- Memory usage increases linearly with body count
- Rendering performance degrades significantly
- File size grows rapidly

**With New Component (Many Bodies):**
- Bodies are grouped and processed as a unit
- Clean timeline with organized operations
- Optimized memory usage through component hierarchy
- Better rendering performance through grouping
- More efficient file structure

**Recommended Usage:**
- **Small Projects (1-10 bodies):** Optional, mainly for organization
- **Medium Projects (10-50 bodies):** Recommended for better performance
- **Large Projects (50+ bodies):** Essential for optimal performance
- **Complex Patterns:** Always use for patterns with many iterations

**Technical Benefits:**
- **Batch Operations:** Multiple bodies processed together
- **Hierarchical Structure:** Better organization in the browser
- **Selective Visibility:** Show/hide entire pattern groups
- **Efficient Updates:** Changes propagate through component hierarchy

**Performance Metrics (Approximate):**

**Memory Usage:**
- **Without Component:** ~2-3MB per 100 bodies
- **With Component:** ~1-1.5MB per 100 bodies (50% reduction)

**Timeline Operations:**
- **Without Component:** 100+ individual operations
- **With Component:** 1-5 grouped operations (95% reduction)

**Rendering Performance:**
- **Without Component:** Linear degradation with body count
- **With Component:** Minimal impact up to 500+ bodies

**File Size:**
- **Without Component:** Grows exponentially with complexity
- **With Component:** Grows linearly with body count

**Best Practices for Large Projects:**
1. **Always enable** "Create New Component" for 20+ bodies
2. **Use descriptive names** for easy identification
3. **Group related patterns** in separate components
4. **Consider component hierarchy** for complex assemblies
5. **Monitor performance** and adjust body count if needed

---

## 🔧 Advanced Features

### Timeline Organization
The plugin automatically creates organized timeline groups:
- **Group Name:** Based on original body name and operation
- **Chronological Order:** Bodies organized sequentially
- **Easy Management:** Expand/collapse groups for clean timeline

### Pattern Creation Strategies

**Spiral Patterns - Best For:**
- Decorative elements and ornaments
- Artistic installations
- Engineering components like springs
- Architectural features
- **Setup:** Rotation priority, same axis for both operations

**Linear Arrays - Best For:**
- Assembly line patterns
- Manufacturing fixtures
- Educational demonstrations
- Prototype development
- **Setup:** Translation priority, zero rotation angle

**Circular Patterns - Best For:**
- Gear assemblies
- Decorative rings
- Mechanical components
- Artistic sculptures
- **Setup:** Zero translation distance, any rotation angle

**Complex Patterns - Best For:**
- Artistic installations
- Advanced engineering components
- Custom decorative elements
- **Setup:** Separate axes, different priorities, creative angle/distance combinations

### Parameter Optimization Tips
- **Spiral Creation:** Combine distance with rotation for spiral effects
- **Linear Arrays:** Use zero rotation for straight lines
- **Circular Patterns:** Use zero distance with rotation
- **Complex Patterns:** Experiment with different angle/distance combinations
- **Parallel Axes:** Similar to traditional spiral behavior
- **Perpendicular Axes:** Creative patterns and arrangements

### Parametric Design Support
The plugin supports parametric expressions in all numeric fields:

**Distance Examples:**
- `d1 * 2` - Double the value of parameter d1
- `spacing + 5 mm` - Add 5mm to spacing parameter
- `width / 3` - Divide width parameter by 3

**Angle Examples:**
- `angle_param + 15 deg` - Add 15° to angle parameter
- `atan(1/2)*180/pi` - Calculate 26.57° using math functions
- `my_angle` - Use parameter name directly

**Pieces Examples:**
- `param + 1` - Add 1 to parameter value
- `count * 2` - Double the count parameter
- `max_pieces` - Use parameter name directly

**Benefits:**
- **Dynamic Updates:** Changes to parameters automatically update the pattern
- **Mathematical Expressions:** Use trigonometry, algebra, and geometry functions
- **Parameter References:** Link to existing Fusion parameters
- **Real-time Preview:** See changes immediately in the dialog

### Parameter Creation and Management

The plugin automatically creates and manages parameters to support parametric design:

**When Parameters Are Created:**
- **Automatic Creation:** When you use the "Name Root" field, the plugin creates a corresponding parameter for the rotation angle
- **Parameter Name:** Uses the same name as your "Name Root" (e.g., "Spiral" creates parameter "Spiral")
- **Parameter Type:** Creates angle parameters in degrees with description "Magic Revolve angle"
- **Existing Parameters:** If a parameter with the same name already exists, the plugin uses the existing one

**How Parameters Are Used:**
- **Rotation Angle:** The created parameter controls the rotation angle for each iteration
- **Iterative Multiplication:** Each body copy uses the parameter multiplied by its iteration number
- **Expression Examples:**
  - First copy: `Spiral * 1` (uses parameter directly)
  - Second copy: `Spiral * 2` (parameter multiplied by 2)
  - Third copy: `Spiral * 3` (parameter multiplied by 3)

**Parameter Integration:**
- **Fusion Integration:** Parameters appear in the Fusion Parameters panel
- **Design Changes:** Modifying the parameter automatically updates all revolved bodies
- **Timeline Updates:** Changes to parameters trigger timeline regeneration
- **Cross-Reference:** Parameters can reference other Fusion parameters

**Example Workflow:**
1. Set "Name Root" to "MySpiral"
2. Plugin creates parameter "MySpiral" with your angle value
3. Each revolved body uses "MySpiral * iteration_number"
4. Change "MySpiral" in Parameters panel → all bodies update automatically

---

## ⚙️ Technical Specifications

### System Requirements
- **Software:** Autodesk® Fusion® (Version 2.0.18000 or later)
- **Operating System:** Windows 10/11, macOS 10.15+
- **Memory:** Minimum 8GB RAM recommended
- **Storage:** 50MB trial space for plugin files

### Performance Guidelines
- **Optimal Body Count:** 10-200 bodies for best performance
- **Large Bodies:** Bodies over 50cm may require longer processing
- **Complex Geometry:** Curved surfaces may increase processing time
- **Memory Usage:** Large body counts consume more system memory

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
- Verify body has proper geometry

**"Translation axis is invalid"**
- Ensure selected edge is linear, sketch line is valid, or construction axis exists
- Verify axis has proper direction and length

**"Rotation axis is invalid"**
- Ensure selected edge is linear, sketch line is valid, or construction axis exists
- Verify axis has proper direction and length

**"Too many bodies requested"**
- Confirm intention for large body count
- Consider performance impact of large operations

**"Revolving operation failed"**
- Check body geometry for errors
- Ensure adequate system memory
- Try simpler geometry or fewer bodies
- Verify axis selections are valid

**Help not working**
- Ensure internet connection is active
- Check firewall settings for browser access
- Try refreshing the help page

### Performance Optimization
- **Close unnecessary applications** before large revolving operations
- **Save your work** before running complex patterns
- **Use Preview mode** to verify settings before execution
- **Consider batch processing** for multiple bodies

---

## 📞 Support and Contact

### Support
- **Email:** jtplugin@ajl.vision
- **Documentation:** This help page and GitHub repository
- **Community:** GitHub Issues and discussions
- **Feature Requests:** Priority consideration for new features
- **Updates:** Automatic through Autodesk App Store

### Additional Resources
- **GitHub Repository:** https://github.com/jtplugin/fusion-magic-revolve
- **Privacy Policy:** https://jtplugin.github.io/privacy-policy
- **Terms of Service:** https://jtplugin.github.io/terms
- **Company Website:** https://github.com/jtplugin

---

## 🔄 Version History

### Version 1.0.0 (Current)
- Initial release with full-featured revolving
- Separate translation and rotation axes
- Operation priority control (Rotation→Translation vs Translation→Rotation)
- Timeline organization
- Custom naming patterns
- Comprehensive validation system
- F1 Help integration

### Planned Features
- Custom path following

---

## 📜 Legal Information

**Copyright © 2025 Giovanni Tommasi - JT Plugin Development**

This software is distributed through the Autodesk App Store under the terms specified in our Terms of Service. By using this plugin, you agree to our Privacy Policy and Terms of Service.

**Privacy:** We respect your privacy. This plugin does not collect or transmit your design data. License verification only transmits machine ID and license key information.

**Support:** For technical support, licensing questions, or feature requests, contact us at jtplugin@ajl.vision

---

*This documentation covers version 1.0.0 of JT Magic Revolve. For the latest updates and features, please check the Autodesk App Store or our GitHub repository.*
