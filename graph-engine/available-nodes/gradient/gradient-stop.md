# Gradient Stop

### What It Does
Creates a gradient stop by pairing a color with a position value. Gradient stops are the building blocks of gradients, defining which colors appear at specific points along the gradient line or radius.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| color | The color at this position in the gradient | Color | Yes |
| position | The location of this color (typically 0-1) | Number | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| gradientStop | The combined gradient stop object (color + position) | Gradient Stop |

### How to Use It
1. Drag the Gradient Stop node into your graph.
2. Connect a color (like `#3366FF`) to the "color" input.
3. Connect or enter a position value (like `0.5` for the middle of the gradient) to the "position" input.
4. Run the graph—your output will be a gradient stop that can be used in a gradient definition.

![Gradient Stop Example](screenshot-placeholder.png)

### Tips
- Position values typically range from 0 (start of gradient) to 1 (end of gradient).
- Create multiple gradient stops and combine them to create a full gradient.

### See Also
- **Create Gradient**: For combining multiple gradient stops into a complete gradient.
- **Color Mix**: For creating intermediate colors that can be used in gradient stops.

### Use Cases
- **Custom Gradients**: Design multi-color gradients with precise control over color positions.
- **Color Transitions**: Define exact transition points between colors in a UI element.
- **Theming**: Create gradient definitions that can adapt to different color schemes. 