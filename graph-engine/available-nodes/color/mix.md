# Mix Colors

### What It Does
Blends two colors together at a specified ratio. This creates smooth transitions between colors and is perfect for generating intermediate shades or creating color relationships.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| colorA | The first color to mix | Color | No |
| colorB | The second color to mix | Color | No |
| value | The mixing ratio (0-1), where 0 is fully colorA and 1 is fully colorB | Number | No |
| space | The color space to perform the mixing in | Text | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The resulting mixed color | Color |

### How to Use It
1. Drag the Mix Colors node into your graph.
2. Connect your first color (like `#3366FF`) to the "colorA" input.
3. Connect your second color (like `#FF9900`) to the "colorB" input.
4. Set a value between 0 and 1 (like `0.5` for an equal mix) to the "value" input.
4. Run the graph—your output will be a blend of the two colors.

![Mix Colors Example](screenshot-placeholder.png)

### Tips
- Different color spaces produce different mixing results. Try "oklch" for perceptually smooth blends.
- To create a color scale, use multiple Mix nodes with different mixing values.

### See Also
- **Color Range**: For creating a series of colors between two endpoints.
- **Lighten/Darken Color**: For simple lightness adjustments to a single color.

### Use Cases
- **Color Harmonies**: Mix complementary colors to create harmonious accent colors.
- **UI State Variations**: Create hover or active states by mixing with white or black.
- **Gradient Development**: Generate intermediate colors for smooth multi-color gradients. 