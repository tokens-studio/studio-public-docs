# Count

### What It Does
Calculates the number of items in an array. It simply returns the length of the input array, regardless of what type of items the array contains.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| value | The array to count items in | List | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The number of items in the array | Number |

### How to Use It
1. Drag the Count node into your graph.
2. Connect an array (like `[10, 20, 30, 40]`) to the "value" input.
3. Run the graph—with the example array, your output will be 4.

![Count Example](screenshot-placeholder.png)

### Tips
- Works with any type of array (numbers, strings, colors, mixed types, etc.).
- Empty arrays will return 0.
- This node counts only the top-level items; it doesn't count items in nested arrays.

### See Also
- **Array Length**: Alternative way to get the length of an array.
- **Filter**: For counting only items that match specific criteria.
- **Array Find**: For locating specific items in an array.

### Use Cases
- **Validation**: Check if an array has any items or has a specific number of items.
- **Dynamic Layouts**: Adjust layouts based on the number of items to display.
- **Data Analysis**: Count the number of data points, colors, or other collection items.
- **Loop Control**: Use the count to determine how many iterations to perform. 