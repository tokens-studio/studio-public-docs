# Scale Vector2

### What It Does
The Scale Vector2 node multiplies a 2D vector by a scalar value, changing its length while preserving its direction. It's useful for resizing vectors or adjusting their magnitude.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Vector | The 2D vector to scale | Vector2 | Yes |
| Scalar | The multiplication factor | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The scaled vector | Vector2 |

### How to Use It
1. Drag the Scale Vector2 node into your graph.
2. Connect a 2D vector (like `[10, 20]`) to the "Vector" input.
3. Set the "Scalar" input to your desired scale factor (like `0.5` or `2`) or use the default (`1`).
4. The output will be a vector with each component multiplied by the scalar (e.g., `[5, 10]` or `[20, 40]`).

![Scale Vector2 Example](screenshot-placeholder.png)

### Tips
- A scalar value of 1 leaves the vector unchanged.
- Negative scalar values reverse the vector's direction.
- Combine with Normalize to create vectors of exact length.

### See Also
- **Normalize Vector2**: For creating a unit vector from any vector.
- **Vector2 Length**: For measuring the magnitude of a vector.

### Use Cases
- **Responsive Design**: Scale dimensions based on screen size or container proportions.
- **Animation**: Adjust movement vectors for speed control.
- **Visual Adjustments**: Resize vector-based graphics while preserving proportions. 