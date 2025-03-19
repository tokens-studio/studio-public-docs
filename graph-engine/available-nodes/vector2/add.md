# Add Vector2

### What It Does
Adds two 2D vectors together by combining their x and y components independently. This is useful for combining positions, velocities, or any pair of values that can be represented as 2D coordinates.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| a | The first vector | Vector2 | Yes |
| b | The second vector | Vector2 | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The sum of vectors a and b | Vector2 |

### How to Use It
1. Drag the Add Vector2 node into your graph.
2. Connect a vector (like `[10, 20]`) to the "a" input.
3. Connect another vector (like `[5, 10]`) to the "b" input.
4. Run the graph—your output will be `[15, 30]`, the sum of both vectors.

![Add Vector2 Example](screenshot-placeholder.png)

### Tips
- Vector addition is commutative—the order of a and b doesn't matter.
- Use this for combining positions, offsets, dimensions, or any paired numeric values.

### See Also
- **Subtract Vector2**: For finding the difference between two vectors.
- **Scale Vector2**: For multiplying a vector by a scalar value.

### Use Cases
- **Position Calculation**: Combine a base position with an offset.
- **Motion Physics**: Add velocity and acceleration vectors together.
- **Layout Design**: Combine width/height dimensions with margin/padding values. 