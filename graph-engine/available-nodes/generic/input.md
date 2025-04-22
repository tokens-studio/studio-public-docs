# Input

### What It Does

Defines the entry points for data flowing into your graph. This node allows you to create named inputs that can be configured when the graph runs, making your graph reusable with different values.

### Inputs

| Name             | Description                                             | Type | Required |
| ---------------- | ------------------------------------------------------- | ---- | -------- |
| \[custom inputs] | Any named inputs you define become available as outputs | Any  | No       |

### Outputs

| Name                | Description                                     | Type |
| ------------------- | ----------------------------------------------- | ---- |
| \[matching outputs] | Each input you define creates a matching output | Any  |

![Input Example](<../../../.gitbook/assets/Screenshot 2025-04-22 at 6.22.55 PM.png>)

### How to Use It

1. Drag the Input node into your graph (usually at the left/beginning).
2. Click the "+" button to add a new named input (like "baseColor" or "spacing").
3. Set the type and default value for each input.
4. Connect the outputs to other nodes in your graph that need these values.
5. When the graph is used, these inputs can be configured externally.

### Tips

* You should only have one Input node per graph.
* Give your inputs clear, descriptive names that indicate their purpose.
* Set meaningful default values so the graph works well even without custom inputs.

### See Also

* **Output**: For defining what values are returned from your graph.
* **Constant**: For values that don't need to change between uses of the graph.

### Use Cases

* **Design System Components**: Create reusable components with configurable properties.
* **Theming**: Build a color scheme generator that takes base colors as inputs.
* **Layout Systems**: Define spacing algorithms that can adapt to different base units.
