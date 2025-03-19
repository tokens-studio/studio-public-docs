# Array Length

### What It Does
Counts how many items are in a list and returns that number. It's perfect for determining the size of collections or arrays.

### Inputs
| Name  | Description                | Type | Required |
|-------|----------------------------|------|----------|
| array | The list to count items in | List | Yes      |

### Outputs
| Name   | Description                   | Type   |
|--------|-------------------------------|--------|
| length | The number of items in the list | Number |

### How to Use It
1. Drag the Array Length node into your graph.
2. Connect your list (like `[Red, Green, Blue]`) to the "array" input.
3. The output will be the number of items in the list (e.g., 3).

![Array Length Example](screenshot-placeholder.png)

### Tips
- An empty array will return 0.
- This node only counts top-level items; it doesn't count elements in nested arrays.

### See Also
- **Count**: For counting specific values in a list.
- **Index Array**: For accessing specific items in a list by their position.

### Use Cases
- **Dynamic Sizing**: Use the length to calculate scalable spacing based on the number of elements.
- **Limit Checking**: Verify if a token collection has the expected number of items.
- **Conditional Logic**: Create different behaviors based on how many items exist in a collection. 