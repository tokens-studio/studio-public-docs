# Name Color

### What It Does
The Name Color node identifies the closest standard CSS color name for any color. It compares the input color to all named web colors and returns the name with the smallest perceptual difference.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Color | The color to identify | Color | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The name of the closest matching CSS color | Text |

### How to Use It
1. Drag the Name Color node into your graph.
2. Connect any color to the "Color" input.
3. The node will automatically find the closest CSS color name.
4. The output will be a string like "steelblue", "mediumorchid", or "firebrick".

![Name Color Example](screenshot-placeholder.png)

### Tips
- This node uses perceptual distance (Delta E) for accurate naming.
- CSS named colors are limited, so the result might not be an exact match.

### See Also
- **String to Color**: For the reverse operation - converting color names to colors.
- **Delta E**: For calculating the difference between colors.

### Use Cases
- **Color Communication**: Convert exact color values to human-readable names for team discussions.
- **Design Documentation**: Generate descriptive color names for design specifications.
- **Data Visualization**: Simplify color data by grouping similar colors under standard names. 