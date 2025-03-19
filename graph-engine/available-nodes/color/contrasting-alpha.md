# Contrasting Alpha

### What It Does
The Contrasting Alpha node adjusts a color's transparency until it reaches a target contrast ratio with a background. It uses binary search to find the optimal alpha value that provides the desired contrast level.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Foreground | The color to adjust transparency for | Color | No |
| Background | The background color to test contrast against | Color | No |
| Algorithm | Contrast calculation method (APCA is default) | Text | No |
| Threshold | Target contrast value to achieve | Number | No |
| Precision | Number of binary search iterations (higher = more precise) | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Alpha | The calculated alpha value (0-1) | Number |
| Color | The resulting color with adjusted transparency | Color |
| Contrast | The actual contrast ratio achieved | Number |

### How to Use It
1. Drag the Contrasting Alpha node into your graph.
2. Connect a foreground color and background color.
3. Set your desired contrast threshold (default: 60).
4. Adjust precision if needed (default: 5 iterations).
5. The node outputs the color with adjusted alpha, the alpha value, and the resulting contrast.

![Contrasting Alpha Example](screenshot-placeholder.png)

### Tips
- Higher precision values give more accurate results but may increase processing time.
- This node is useful for ensuring text remains readable while maintaining some transparency.

### See Also
- **Contrast**: For measuring contrast between two colors.
- **Contrasting**: For selecting between two colors based on contrast.
- **Flatten Alpha**: For removing transparency from a color.

### Use Cases
- **Semi-Transparent UI Elements**: Create overlay panels that maintain text readability.
- **Accessible Design**: Ensure text with transparency meets accessibility standards.
- **Dynamic Backgrounds**: Automatically adjust text opacity based on varying background colors. 