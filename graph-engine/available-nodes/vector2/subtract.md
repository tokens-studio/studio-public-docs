# Subtract Vector2

### What It Does
The Subtract Vector2 node calculates the difference between two 2D vectors. It's useful for finding displacement vectors between points or reversing vector operations.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| A | First vector (minuend) | Vector2 | Yes |
| B | Second vector to subtract (subtrahend) | Vector2 | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The result of A - B | Vector2 |

### How to Use It
1. Drag the Subtract Vector2 node into your graph.
2. Connect your first vector to the "A" input.
3. Connect your second vector to the "B" input.
4. The output will be the vector difference ([A.x - B.x, A.y - B.y]).

![Subtract Vector2 Example](screenshot-placeholder.png)

### Tips
- Subtracting vector B from A gives you the displacement vector from B to A.
- The order matters: A - B is not the same as B - A (they point in opposite directions).

### See Also
- **Add Vector2**: For combining two vectors.
- **Scale Vector2**: For multiplying a vector by a scalar value.

### Use Cases
- **Displacement Calculation**: Find the vector needed to move from one point to another.
- **Relative Positioning**: Calculate positions relative to reference points.
- **Motion Adjustment**: Compensate for existing movement by applying an opposing vector. 