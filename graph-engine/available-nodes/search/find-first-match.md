# Find First Match

### What It Does
Searches through a list of numbers to find the first item that satisfies a specified comparison with a target value. It can find values greater than or less than a specified number and returns both the matching value and its position.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| array | The list of numbers to search through | List | Yes |
| target | The comparison value to test against | Number | Yes |
| operator | The comparison type (">" for greater than or "<" for less than) | Text | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The first matching value found (undefined if none found) | Number |
| index | The position of the matching value in the array (-1 if none found) | Number |
| found | Whether a matching value was found | Yes/No |

### How to Use It
1. Drag the Find First Match node into your graph.
2. Connect an array of numbers (like `[5, 10, 15, 20]`) to the "array" input.
3. Set a target number (like `12`) to the "target" input.
4. Choose an operator (like `>` to find values greater than the target).
5. Run the graph—with the example inputs, your output will be: value: `15`, index: `2`, found: `true`.

![Find First Match Example](screenshot-placeholder.png)

### Tips
- Always check the "found" output before using the value, as it may be undefined if no match was found.
- The search stops at the first matching item, even if multiple items would match.

### See Also
- **Array Find**: For more complex finding conditions using an inner graph.
- **Array Filter**: For getting all items that match a condition instead of just the first.

### Use Cases
- **Threshold Detection**: Find the first value that exceeds a minimum threshold.
- **Breakpoint Identification**: Locate the first screen width breakpoint that's smaller than the current viewport.
- **Financial Analysis**: Find the first data point where a value crosses above or below a critical level. 