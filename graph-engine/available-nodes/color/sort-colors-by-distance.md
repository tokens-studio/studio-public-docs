# Sort Colors By Distance

### What It Does
The Sort Colors By Distance node arranges an array of colors by their relationship to a reference color. It can sort based on various color attributes like contrast, hue, lightness, saturation, or overall color distance.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Colors | Array of colors to be sorted | List of Colors | Yes |
| Compare Color | Reference color to sort against | Color | Yes |
| Type | Sorting method (Contrast, Hue, Lightness, Saturation, Distance) | Text | No |
| Algorithm | Contrast algorithm to use when sorting by contrast | Text | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The sorted array of colors | List of Colors |
| Indices | The original indices of the colors in the sorted array | List of Numbers |

### How to Use It
1. Drag the Sort Colors By Distance node into your graph.
2. Connect an array of colors to the "Colors" input.
3. Connect a reference color to the "Compare Color" input.
4. Select a sorting method from the "Type" dropdown (default: Hue).
5. The output will be the sorted colors and their original indices.

![Sort Colors By Distance Example](screenshot-placeholder.png)

### Tips
- Use different sorting methods to achieve various visual arrangements of color palettes.
- The indices output is useful for tracking how the original array was rearranged.

### See Also
- **Color Wheel**: For generating colors to sort.
- **Range**: For creating color ranges to sort.

### Use Cases
- **Color Palette Organization**: Arrange colors in a visually logical order.
- **Accessible Color Selection**: Sort by contrast to find the most readable options.
- **Gradient Generation**: Sort colors by hue or lightness to create smooth transitions. 