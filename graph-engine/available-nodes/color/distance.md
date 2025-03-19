# Distance

### What It Does
The Distance node measures the geometric distance between two colors in a specified color space. Unlike Delta E, which measures perceptual difference, this node calculates raw mathematical distance between color coordinates.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Color A | First color for distance calculation | Color | No |
| Color B | Second color for distance calculation | Color | No |
| Precision | Number of decimal places in the result | Number | No |
| Space | Color space to perform calculation in (Lab, ICtCp, Jzazbz) | Text | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The calculated distance between the colors | Number |

### How to Use It
1. Drag the Distance node into your graph.
2. Connect two colors to "Color A" and "Color B" inputs.
3. Select a color space (default is "Lab").
4. Set the desired precision for the result (default is 4 decimal places).
5. The output value indicates the geometric distance between the colors.

![Distance Example](screenshot-placeholder.png)

### Tips
- Different color spaces produce different results as they represent color differently.
- Lab is generally a good default space for most design applications.
- Higher values indicate greater distance/difference between colors.

### See Also
- **Delta E**: For calculating perceptually accurate color differences.
- **Sort Colors By Distance**: For sorting colors based on their differences.
- **Contrast**: For calculating contrast ratio between colors.

### Use Cases
- **Color Sorting**: Organize colors based on their distance from a reference color.
- **Color Difference Analysis**: Compare color similarity in mathematical terms.
- **Color Space Exploration**: Understand how colors relate in different color spaces. 