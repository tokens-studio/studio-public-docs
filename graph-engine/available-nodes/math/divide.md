# Divide

### What It Does
Divides one number by another, producing their quotient. This basic math operation is useful for scaling, calculating proportions, or determining ratios between values.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| a | The dividend (number being divided) | Number | Yes |
| b | The divisor (number to divide by) | Number | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The quotient (a divided by b) | Number |

### How to Use It
1. Drag the Divide node into your graph.
2. Connect a number (like `10`) to the "a" input.
3. Connect another number (like `2`) to the "b" input.
4. Run the graph—your output will be `5`.

![Divide Example](screenshot-placeholder.png)

### Tips
- Be careful with division by zero, which results in Infinity or NaN (not a number).
- Use division to create proportional relationships between values.

### See Also
- **Multiply**: For multiplying numbers together.
- **Reciprocal**: For calculating 1/x (if available).

### Use Cases
- **Scale Calculation**: Convert between different measurement units (e.g., pixels to percentages).
- **Aspect Ratios**: Calculate width-to-height ratios for responsive elements.
- **Distribution**: Divide a total value evenly among multiple elements. 