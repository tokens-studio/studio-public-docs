# Fluid

### What It Does
The Fluid node calculates responsive values that smoothly scale between minimum and maximum sizes based on the viewport width. It's perfect for creating fluid typography, spacing, and other responsive design elements.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Min Size | Minimum size in pixels | Number | No |
| Max Size | Maximum size in pixels | Number | No |
| Min Viewport | Minimum viewport width in pixels | Number | No |
| Max Viewport | Maximum viewport width in pixels | Number | No |
| Viewport | Current viewport width in pixels | Number | No |
| Precision | Number of decimal places in the output | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The calculated fluid value | Number |

### How to Use It
1. Drag the Fluid node into your graph.
2. Set your size range (defaults: Min Size 16px, Max Size 24px).
3. Set your viewport range (defaults: Min Viewport 320px, Max Viewport 1920px).
4. Connect a viewport width or use the default (768px).
5. The output will give you a proportionally scaled value between your min and max sizes.

![Fluid Example](screenshot-placeholder.png)

### Tips
- The value is automatically clamped to stay within your min and max size range.
- You can reverse the scaling effect by setting min size larger than max size.

### See Also
- **Lerp**: For linear interpolation between two values.
- **Range Mapping**: For mapping values from one range to another.

### Use Cases
- **Responsive Typography**: Create text that grows smoothly from mobile to desktop.
- **Fluid Spacing**: Scale spacing values based on screen size for consistent layouts.
- **Adaptive Components**: Design elements that resize proportionally to the viewport. 