# Arithmetic Series

### What It Does
The Arithmetic Series node generates a sequence of numbers where each value increases or decreases by a constant amount. It creates evenly-spaced numerical progressions for scales, grids, and other design patterns.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Base | The central value of the series | Number | No |
| Steps Down | Number of steps to generate below the base value | Number | No |
| Steps Up | Number of steps to generate above the base value | Number | No |
| Increment | The constant value to add/subtract between steps | Number | No |
| Precision | Number of decimal places for the output values | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Array | The resulting sequence of numbers | List |
| Indexed | Array of objects with index and value properties | List |

### How to Use It
1. Drag the Arithmetic Series node into your graph.
2. Set the "Base" value (default: 16) as the center point of your series.
3. Configure "Steps Down" (default: 0) and "Steps Up" (default: 1) to control series length.
4. Adjust the "Increment" (default: 1) to set spacing between values.

![Arithmetic Series Example](screenshot-placeholder.png)

### Tips
- The "Steps Down" parameter generates values below your base (smaller values).
- The "Steps Up" parameter generates values above your base (larger values).

### See Also
- **Geometric Series**: For creating exponential progressions where values multiply by a ratio.
- **Linear Space**: For creating evenly spaced values between specific endpoints.

### Use Cases
- **Spacing Systems**: Create evenly-spaced size tokens for layout grids (4, 8, 12, 16, 20, 24).
- **Font Size Scales**: Generate linear type scales (12, 14, 16, 18, 20px).
- **Color Steps**: Define evenly-spaced opacity or intensity values (0.2, 0.4, 0.6, 0.8). 