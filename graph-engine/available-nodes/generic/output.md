# Output

### What It Does

Defines the final results that your graph produces. This node collects values from within your graph and exposes them as named outputs, determining what data is returned when the graph completes.

### Inputs

| Name             | Description                                       | Type | Required |
| ---------------- | ------------------------------------------------- | ---- | -------- |
| \[custom inputs] | Any named inputs you add become the graph outputs | Any  | No       |

### Outputs

| Name                | Description                                                      | Type |
| ------------------- | ---------------------------------------------------------------- | ---- |
| \[matching outputs] | Each input creates a matching output (typically used internally) | Any  |

![Output Example](<../../../.gitbook/assets/Screenshot 2025-04-22 at 6.29.51 PM.png>)

### How to Use It

1. Drag the Output node into your graph (usually at the right/end).
2. Click the "+" button to add named inputs (like "resultColor" or "spacingScale").
3. Connect values from your graph to these inputs.
4. When the graph runs, these connected values will be available as the graph's outputs.

### Tips

* You should only have one Output node per graph.
* Give your outputs clear, descriptive names that indicate what they contain.
* Every value you want to access from outside the graph should connect to this node.

### See Also

* **Input**: For defining entry points where data flows into your graph.
* **Constant**: For fixed values that don't change during graph execution.

### Use Cases

* **Token Generation**: Export the final set of design tokens after processing.
* **Calculation Results**: Return the results of complex calculations or transformations.
* **Component APIs**: Define what properties a reusable graph component exposes.
