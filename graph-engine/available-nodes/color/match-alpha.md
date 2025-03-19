# Match Alpha

### What It Does
The Match Alpha node calculates the opacity value needed to blend a foreground color with a background color to match a reference color. It reverse-engineers the alpha value that would create the target color.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Foreground | The color to apply transparency to | Color | No |
| Background | The background color for blending | Color | No |
| Reference | The target color to match | Color | No |
| Threshold | Maximum allowable color difference (0-1) | Number | No |
| Precision | Calculation precision for alpha value | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| In Range | Whether a valid alpha value was found | Yes/No |
| Color | The foreground color with the calculated alpha | Color |
| Alpha | The calculated alpha value (0-1) | Number |

### How to Use It
1. Drag the Match Alpha node into your graph.
2. Connect your foreground color, background color, and reference color.
3. Adjust threshold and precision if needed (defaults are 0.01).
4. The node outputs the calculated alpha value and the semi-transparent foreground color.
5. If "In Range" is false, no suitable alpha value could be found.

![Match Alpha Example](screenshot-placeholder.png)

### Tips
- Lower threshold values require more exact color matching.
- If no suitable alpha is found, try different foreground and background colors.
- This node works best when the reference color is between the foreground and background colors.

### See Also
- **Flatten Alpha**: For the reverse operation - merging a transparent color with a background.
- **Contrasting Alpha**: For finding alpha values that maintain contrast requirements.

### Use Cases
- **Color System Analysis**: Discover the transparency values used in existing designs.
- **Overlay Recreation**: Recreate the exact transparency of an existing overlay or glass effect.
- **Color Harmonization**: Find transparency values that harmonize colors in a composition. 