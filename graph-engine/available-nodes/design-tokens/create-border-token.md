---
hidden: true
---

# Create Border Token

### What It Does

The Create Border Design Token node creates a complete border token by combining a name with border value(s) or a reference. It's used to define standardized borders in your design system.

### Inputs

| Name        | Description                                            | Type   | Required |
| ----------- | ------------------------------------------------------ | ------ | -------- |
| Name        | The token's identifier                                 | Text   | Yes      |
| Reference   | Reference to another token (if not using direct value) | Text   | No\*     |
| Value       | Array of border values (color, width, style)           | List   | No\*     |
| Description | Optional explanation of the token's purpose            | Text   | No       |
| $extensions | Additional metadata for the token                      | Object | No       |

\*Either Reference or Value must be provided

### Outputs

| Name  | Description                      | Type  |
| ----- | -------------------------------- | ----- |
| Token | The complete border design token | Token |

### How to Use It

1. Drag the Create Border Design Token node into your graph.
2. Connect a name (like "border.primary") to the "Name" input.
3. Either connect border value(s) from Create Border nodes to the "Value" input, or
4. Connect a reference string (like "{border.base}") to the "Reference" input.
5. Optionally add a description and extensions as needed.

![Create Border Design Token Example](screenshot-placeholder.png)

### Tips

* Use Value for direct border definitions, or Reference to point to another border token.
* You can provide multiple border values to create complex borders.

### See Also

* **Create a Border**: For creating border values to use with this node.
* **Create Design Token**: For creating basic design tokens of other types.

### Use Cases

* **Component Library**: Define standard borders for UI elements like buttons and cards.
* **Design System**: Create a consistent set of border tokens for various states and components.
* **Theme Switching**: Create border tokens that can be swapped out for different themes.
