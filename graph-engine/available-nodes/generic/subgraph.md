# Subgraph

### What It Does
Creates a nested graph within your main graph, allowing you to encapsulate complex logic into a reusable component. It acts like a function that can contain its own internal network of nodes.

### Inputs
| Name     | Description                                | Type | Required |
|----------|--------------------------------------------|------|----------|
| (dynamic) | Inputs are defined by the inner graph's Input nodes | Any | Depends on inner graph |

### Outputs
| Name     | Description                                | Type |
|----------|--------------------------------------------|------|
| (dynamic) | Outputs are defined by the inner graph's Output nodes | Any |

### How to Use It
1. Drag the Subgraph node into your graph.
2. Double-click the node to open and edit the inner graph.
3. Add Input and Output nodes within the inner graph to define the interface.
4. Build your logic inside the subgraph using any other nodes.

![Subgraph Example](screenshot-placeholder.png)

### Tips
- Keep related functionality together by grouping it in a subgraph for better organization.
- Inputs and outputs from the inner graph automatically appear on the parent subgraph node.

### See Also
- **Input**: For defining inputs to your graph.
- **Output**: For defining outputs from your graph.

### Use Cases
- **Reusable Components**: Create complex operations that can be reused across different parts of your design system.
- **Logical Grouping**: Organize related nodes into a single component to reduce visual complexity.
- **Abstraction**: Hide implementation details of complex calculations behind a simpler interface. 