# Array Map

### What It Does
Transforms each item in a list by applying the same operations to every element. It runs a mini-graph for each item in your list and collects the results into a new list of the same length.

### Inputs
| Name  | Description                   | Type | Required |
|-------|-------------------------------|------|----------|
| array | The list to process each item | List | Yes      |
| *Dynamic inputs* | Any inputs you add to the inner graph will appear here | Varies | No |

### Outputs
| Name  | Description                                 | Type |
|-------|---------------------------------------------|------|
| value | The resulting list after processing each item | List |

### Inner Graph Special Inputs
| Name | Description | Type |
|------|-------------|------|
| value | The current array item being processed | Any |
| index | The current position in the array | Number |
| length | The total length of the array | Number |

### Inner Graph Required Output
| Name | Description | Type |
|------|-------------|------|
| value | The transformed value to include in the result array | Any |

### How to Use It
1. Drag the Array Map node into your graph.
2. Connect your list (like `[10, 20, 30]`) to the "array" input.
3. Double-click the node to open the inner graph editor.
4. Inside the inner graph, build your transformation logic using the "value" input.
5. Connect your transformed result to the "value" output on the Output node.
6. Return to the main graph, where you can use the transformed array output.

![Array Map Example](screenshot-placeholder.png)

### Tips
- The inner graph runs once for each item in the array, in order.
- You can add your own inputs to the inner graph's Input node, which will appear as inputs on the main Array Map node.
- Use "index" inside the inner graph to access the position of the current item being processed.
- The resulting array will always have the same length as the input array.

### See Also
- **Array Filter**: For selecting only specific items from a list rather than transforming all of them.
- **Array Find**: For finding a single item in an array based on custom criteria.
- **Array Subgraph**: For more complex list processing operations that need nested logic.

### Use Cases
- **Color Palette Generation**: Transform a list of base colors by applying the same adjustments to each.
- **Scaling Values**: Convert all measurements in a list by applying the same mathematical operations.
- **Token Transformation**: Process each design token in a collection to add or modify properties consistently. 