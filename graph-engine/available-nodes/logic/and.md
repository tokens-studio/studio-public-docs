# Logical AND

### What It Does
Checks if all connected inputs are true and returns a single true/false result. It's perfect for combining multiple conditions that all need to be met before proceeding with an action.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| inputs | Multiple values to check (can add as many as needed) | Any | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | True if all inputs are true/truthy, false otherwise | Yes/No |

### How to Use It
1. Drag the Logical AND node into your graph.
2. Click the "+" button to add as many input connections as you need.
3. Connect boolean values or conditions to each input.
4. Run the graph—your output will be true only if all inputs are true.

![Logical AND Example](screenshot-placeholder.png)

### Tips
- Non-boolean values are converted to boolean: empty values, zero, null, and undefined become false.
- An AND node with no inputs will return true (similar to mathematical product of an empty set).

### See Also
- **Logical OR**: For checking if at least one condition is true.
- **NOT**: For inverting a boolean value.

### Use Cases
- **Validation Rules**: Check if a color meets multiple criteria (high enough contrast AND within brand palette).
- **Complex Conditions**: Enable a feature only when multiple requirements are met.
- **Design States**: Apply a style only when an element is both hovered AND active. 