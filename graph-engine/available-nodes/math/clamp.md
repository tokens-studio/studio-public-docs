# Clamp

### What It Does
Restricts a value to stay within a specified minimum and maximum range. If the value is below the minimum, it returns the minimum; if it's above the maximum, it returns the maximum; otherwise, it returns the original value.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| value | The number to clamp | Number | No |
| min | The lower boundary | Number | No |
| max | The upper boundary | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The clamped result | Number |

### How to Use It
1. Drag the Clamp node into your graph.
2. Set "value" to the number you want to restrict (e.g., 25).
3. Set "min" to the lower bound (e.g., 0).
4. Set "max" to the upper bound (e.g., 10).
5. Run the graph—with the example values, your output will be 10 (since 25 exceeds the max).

![Clamp Example](screenshot-placeholder.png)

### Tips
- Make sure min is less than max, or the clamp will always return the min value.
- Clamp is useful for ensuring values stay within valid ranges before passing to other nodes.
- For colors and other non-numeric values, use specialized constraint nodes instead.

### See Also
- **Min**: For finding the minimum of multiple values.
- **Max**: For finding the maximum of multiple values.
- **Range Mapping**: For transforming values from one range to another.

### Use Cases
- **Boundary Enforcement**: Ensure values stay within acceptable limits.
- **Input Validation**: Sanitize user inputs to prevent extreme values.
- **Responsive Sizing**: Limit element sizes between minimum and maximum constraints.
- **Animation Control**: Prevent objects from moving outside defined areas. 