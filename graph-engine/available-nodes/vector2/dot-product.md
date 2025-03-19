# Dot Product Vector2

### What It Does
The Dot Product Vector2 node calculates the scalar product of two 2D vectors. It's useful for determining the angle between vectors or projecting one vector onto another.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| A | First 2D vector | Vector2 | Yes |
| B | Second 2D vector | Vector2 | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The dot product result | Number |

### How to Use It
1. Drag the Dot Product Vector2 node into your graph.
2. Connect your first vector to the "A" input.
3. Connect your second vector to the "B" input.
4. The output will be the dot product, calculated as A.x * B.x + A.y * B.y.

![Dot Product Vector2 Example](screenshot-placeholder.png)

### Tips
- A dot product of 0 means the vectors are perpendicular (at 90° to each other).
- The dot product is positive when vectors point in similar directions, negative when they point in opposite directions.

### See Also
- **Length**: For calculating the magnitude of a vector.
- **Normalize**: For converting a vector to a unit vector while preserving direction.

### Use Cases
- **Direction Comparison**: Determine if vectors are pointing in similar or opposite directions.
- **Projection Calculations**: Find the component of one vector in the direction of another.
- **Angle Detection**: Use in conjunction with vector lengths to determine the angle between vectors. 