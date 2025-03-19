# Difference

### What It Does
The Difference node calculates the absolute difference between two numbers. It's useful for measuring the gap between values while disregarding which is larger.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| A | First number in the comparison | Number | No |
| B | Second number in the comparison | Number | No |
| Precision | How many decimal places to round to | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Difference | The absolute difference between A and B | Number |

### How to Use It
1. Drag the Difference node into your graph.
2. Connect your first number to the "A" input or use the default (0).
3. Connect your second number to the "B" input or use the default (0).
4. Optionally set the "Precision" input (defaults to 2 decimal places).

![Difference Example](screenshot-placeholder.png)

### Tips
- The result is always positive, regardless of which input is larger.
- Use the precision input to control rounding (e.g., 0 for integers, 2 for cents).

### See Also
- **Abs**: For getting the absolute value of a single number.
- **Subtract**: For getting the signed difference between numbers.

### Use Cases
- **Contrast Measurement**: Calculate the difference between foreground and background colors.
- **Error Margins**: Determine how far a value deviates from a target.
- **Spacing Consistency**: Check the difference between actual and intended spacing values. 