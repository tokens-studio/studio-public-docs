# Create Vector2

### What It Does
Creates a 2D vector from x and y coordinate values. A 2D vector represents both direction and magnitude, useful for positions, dimensions, or movements in a 2D space.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| x | The horizontal component of the vector | Number | Yes |
| y | The vertical component of the vector | Number | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The created 2D vector | Vector2 |

### How to Use It
1. Drag the Create Vector2 node into your graph.
2. Connect or enter a number for the "x" input.
3. Connect or enter a number for the "y" input.
4. Run the graph—your output will be a 2D vector containing both values.

![Create Vector2 Example](screenshot-placeholder.png)

### Tips
- Vectors are represented as [x, y] arrays but have special properties when used with vector operations.
- Use this node when you need to work with positions, directions, or sizes in 2D space.

### See Also
- **Vector2 Add**: For combining two vectors together.
- **Vector2 Destructure**: For breaking a vector into its x and y components.

### Use Cases
- **Position Calculations**: Create position vectors for layout algorithms.
- **Size Definition**: Define width and height as a vector for aspect ratio calculations.
- **Direction Vectors**: Create normalized direction vectors for animations or gradients. 