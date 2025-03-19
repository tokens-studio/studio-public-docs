# Contrasting from Array

### What It Does
The Contrasting from Array node evaluates multiple colors against a background and returns the first one that meets a contrast threshold. If no color is sufficiently contrasting, it returns the one with the highest contrast.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Colors | Array of color options to evaluate | List of Colors | Yes |
| Background | The background color to test contrast against | Color | No |
| Algorithm | Contrast calculation method (APCA is default) | Text | No |
| Threshold | Minimum contrast value considered sufficient (default: 60) | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Color | The selected color with best/sufficient contrast | Color |
| Sufficient | Whether the selected color meets the threshold | Yes/No |
| Contrast | The contrast ratio of the selected color | Number |
| Index | The position of the selected color in the original array | Number |

### How to Use It
1. Drag the Contrasting from Array node into your graph.
2. Connect an array of colors to the "Colors" input.
3. Set the "Background" to the surface color where the colors will appear.
4. Adjust the "Threshold" to your desired minimum contrast level.
5. The node outputs the first color that meets the threshold, or the one with highest contrast.

![Contrasting from Array Example](screenshot-placeholder.png)

### Tips
- Arrange your colors array with preferred options first, as the node returns the first sufficient color.
- The index output is useful for tracking which color was selected from the array.

### See Also
- **Contrasting**: For choosing between two specific colors.
- **Contrast**: For calculating the contrast ratio between colors.
- **Sort Colors By Distance**: For ordering colors by their contrast.

### Use Cases
- **Theme Color Selection**: Find an appropriate color from a theme palette for a specific background.
- **Text Color Optimization**: Automatically select the most readable text color from a set of brand options.
- **Accessible UI Components**: Choose colors that meet accessibility requirements from a predefined set. 