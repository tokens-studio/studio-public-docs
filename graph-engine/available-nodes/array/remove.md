# Remove Item

### What It Does
Removes a single item from a list at a specific position. It returns both the modified list and the item that was removed, making it useful for extracting elements or trimming collections.

### Inputs
| Name  | Description                            | Type   | Required |
|-------|----------------------------------------|--------|----------|
| array | The list to remove an item from       | List   | Yes      |
| index | The position of the item to remove     | Number | Yes      |

### Outputs
| Name  | Description                            | Type   |
|-------|----------------------------------------|--------|
| array | The list with the item removed         | List   |
| item  | The item that was removed              | Any    |

### How to Use It
1. Drag the Remove Item node into your graph.
2. Connect a list (like `[Red, Blue, Green]`) to the "array" input.
3. Connect a number (like `1`) to the "index" input to specify which position to remove.
4. Run the graph—your "array" output will be `[Red, Green]` and your "item" output will be `Blue`.

![Remove Item Example](screenshot-placeholder.png)

### Tips
- Indexes start at 0, so the first item is at position 0, the second at position 1, etc.
- You can use negative indexes (-1 removes the last item, -2 the second-to-last, etc.).

### See Also
- **Array Push**: For adding an item to a list.
- **Array Filter**: For removing multiple items based on conditions.

### Use Cases
- **Token Refinement**: Remove specific tokens from a design system collection to create simplified subsets.
- **Data Processing**: Extract a specific element from a data series for individual analysis.
- **Sequential Operations**: Process items one-by-one by removing them from a working list as you handle them. 