# Normalize Vector2

### What It Does
The Normalize Vector2 node converts a 2D vector to a unit vector (magnitude of 1) while preserving its direction. It's essential for working with direction vectors in animations and layouts.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Vector | The 2D vector to normalize | Vector2 | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The normalized unit vector | Vector2 |

### How to Use It
1. Drag the Normalize Vector2 node into your graph.
2. Connect a 2D vector (like `[3, 4]`) to the "Vector" input.
3. The output will be a vector pointing in the same direction but with length 1 (e.g., `[0.6, 0.8]`).
4. Use this for direction-only operations where magnitude should be consistent.

![Normalize Vector2 Example](screenshot-placeholder.png)

### Tips
- If the input vector is `[0, 0]` (zero vector), the output will also be `[0, 0]` since it has no direction.
- Normalizing before scaling gives you precise control over vector magnitude.

### See Also
- **Vector2 Length**: For calculating the magnitude of a vector.
- **Scale Vector2**: For adjusting the magnitude of a vector.

### Use Cases
- **Direction Vectors**: Create consistent direction indicators for UI elements.
- **Movement Controls**: Normalize input vectors to ensure consistent movement speed.
- **Visual Indicators**: Generate evenly-sized directional markers or arrows. 