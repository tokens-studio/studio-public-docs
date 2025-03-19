# Evaluate math

### What It Does
The Evaluate math node calculates the result of arbitrary mathematical expressions using variables. It lets you create complex formulas combining multiple values without needing multiple math nodes.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Expression | Mathematical formula to evaluate | Text | Yes |
| [Variables] | Custom inputs used in the expression | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The calculated result of the expression | Number |
| Expression | The expression that was evaluated | Text |

### How to Use It
1. Drag the Evaluate math node into your graph.
2. Enter a mathematical expression like `"a * 2 + b"` in the "Expression" input.
3. Add input variables by name (in this case, connect values to inputs "a" and "b").
4. The node will calculate the result based on your formula and connected values.

![Evaluate Math Example](screenshot-placeholder.png)

### Tips
- Supports standard operators (+, -, *, /, ^), functions (sin, cos, sqrt), and constants (pi, e).
- Variable names in your expression must match the input names you add to the node.

### See Also
- **Add (Variadic)**: For simpler addition of multiple values.
- **Multiply (Variadic)**: For simpler multiplication of multiple values.

### Use Cases
- **Complex Calculations**: Create custom formulas like `"width * 0.75 - padding * 2"` for layout logic.
- **Design Algorithms**: Implement specific design calculations such as contrast ratios.
- **Responsive Scaling**: Create expressions that adjust values based on multiple parameters. 