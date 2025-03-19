# Array Filter

### What It Does
Creates a new list containing only the items that meet specific conditions. It runs a test on each item and keeps only those that pass, perfect for filtering token collections based on criteria.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| array | The list of items to filter | List | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The filtered list containing only items that met the condition | List |

### How to Use It
1. Drag the Array Filter node into your graph.
2. Connect your source list to the "array" input.
3. Double-click the node to open the inner filter graph.
4. Create a condition in the inner graph that returns true for items you want to keep.
4. Run the graph—your output will be a new list with only the matching items.

![Array Filter Example](screenshot-placeholder.png)

### Tips
- The inner filter graph has special inputs: "value" (current item), "index" (position), and "length" (total count).
- Connect your logic to the "matches" output in the inner graph to define which items to keep.

### See Also
- **Array Find**: For finding just the first matching item in a list.
- **Array Remove**: For removing specific items from a list.

### Use Cases
- **Filtered Color Palettes**: Keep only colors that meet a specific brightness threshold for light/dark themes.
- **Token Subset**: Filter spacing tokens to only include values within a certain range.
- **Data Filtering**: Remove unwanted values from a data list before visualization or processing. 