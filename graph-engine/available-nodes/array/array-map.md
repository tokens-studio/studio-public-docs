# Array Map

### What It Does
Transforms each item in a list by applying the same operations to every element. It runs a mini-graph for each item in your list and collects the results into a new list of the same length.

### Inputs
| Name  | Description                   | Type | Required |
|-------|-------------------------------|------|----------|
| array | The list to process each item | List | Yes      |

### Outputs
| Name  | Description                                 | Type |
|-------|---------------------------------------------|------|
| value | The resulting list after processing each item | List |

### How to Use It
1. Drag the Array Map node into your graph.
2. Connect your list (like `[10, 20, 30]`) to the "array" input.
3. Double-click the node to open the inner graph editor.
4. Inside the inner graph, build your transformation logic between the input and output nodes.

![Array Map Example](screenshot-placeholder.png)

### Tips
- The inner graph automatically has "value", "index", and "length" inputs available.
- Use "index" inside the inner graph to access the position of the current item being processed.

### See Also
- **Array Filter**: For selecting only specific items from a list rather than transforming all of them.
- **Array Subgraph**: For more complex list processing operations that need nested logic.

### Use Cases
- **Color Palette Generation**: Transform a list of base colors by applying the same adjustments to each.
- **Scaling Values**: Convert all measurements in a list by applying the same mathematical operations.
- **Token Transformation**: Process each design token in a collection to add or modify properties consistently. 