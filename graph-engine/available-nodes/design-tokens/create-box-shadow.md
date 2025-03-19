# Create a Box Shadow

### What It Does
The Create a Box Shadow node generates a composite box shadow value by combining x, y, blur, spread, color, and type properties. It's used to define consistent shadow effects in your design system.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| X | Horizontal offset of the shadow (e.g., "0px" or "2px") | Text | Yes |
| Y | Vertical offset of the shadow (e.g., "2px" or "4px") | Text | Yes |
| Blur | Shadow blur radius (e.g., "5px" or "10px") | Text | Yes |
| Spread | Shadow spread distance (e.g., "0px" or "2px") | Text | Yes |
| Color | Shadow color (e.g., "rgba(0,0,0,0.2)" or "#00000033") | Text | Yes |
| Type | Shadow type: "innerShadow" or "dropShadow" | Text | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The composite box shadow value | Box Shadow |

### How to Use It
1. Drag the Create a Box Shadow node into your graph.
2. Connect x offset (like "0px") to the "X" input.
3. Connect y offset (like "4px") to the "Y" input.
4. Connect blur radius (like "8px") to the "Blur" input.
5. Connect spread distance (like "0px") to the "Spread" input.
6. Connect color value (like "rgba(0,0,0,0.15)") to the "Color" input.
7. Connect shadow type (like "dropShadow") to the "Type" input.

![Create a Box Shadow Example](screenshot-placeholder.png)

### Tips
- Use "dropShadow" for outer shadows and "innerShadow" for inner shadows.
- Use RGBA or hex with alpha for shadows to control opacity separately from color.

### See Also
- **Create Box Shadow Token**: For creating a complete box shadow token with name and metadata.
- **Create Design Token**: For creating other types of design tokens.

### Use Cases
- **Elevation System**: Create consistent shadow values for different elevation levels.
- **Interactive States**: Define shadows for hover, active, or focus states.
- **Modal Overlays**: Create shadows for modals, dialogs, and popups.