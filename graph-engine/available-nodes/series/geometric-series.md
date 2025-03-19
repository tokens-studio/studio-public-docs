# Geometric Series

### What It Does
The Geometric Series node generates a sequence where each number is multiplied by a constant ratio. It creates exponential progressions perfect for scales that require accelerating or decelerating growth.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Base | The central value of the series | Number | No |
| Steps Down | Number of steps to generate below the base value | Number | No |
| Steps Up | Number of steps to generate above the base value | Number | No |
| Ratio | The multiplier between consecutive values | Number | No |
| Precision | Number of decimal places for the output values | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Array | The resulting sequence of numbers | List |
| Indexed | Array of objects with index and value properties | List |

### How to Use It
1. Drag the Geometric Series node into your graph.
2. Set the "Base" value (default: 16) as the center point of your series.
3. Configure "Steps Down" (default: 0) and "Steps Up" (default: 1) to control series length.
4. Adjust the "Ratio" (default: 1.5) to set the multiplier between values.

![Geometric Series Example](screenshot-placeholder.png)

### Tips
- With ratio > 1, values increase exponentially as you move up from the base.
- With ratio < 1 but > 0, values decrease exponentially as you move up from the base.

### See Also
- **Arithmetic Series**: For creating linear progressions with constant differences.
- **Power Series**: For creating progressions based on powers of a number.

### Use Cases
- **Type Scales**: Create font size systems with meaningful proportional relationships (8, 12, 18, 27, 40.5).
- **Spacing Systems**: Define spacing tokens with accelerating growth (4, 8, 16, 32, 64).
- **Visual Hierarchy**: Generate size scales that create clear visual distinctions between elements. 