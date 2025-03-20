---
hidden: true
---

# Create Typography Token

### What It Does

The Create Typography Design Token node creates a complete typography token by combining a name with typography value(s) or a reference. It's used to define standardized text styles in your design system.

### Inputs

| Name        | Description                                            | Type       | Required |
| ----------- | ------------------------------------------------------ | ---------- | -------- |
| Name        | The token's identifier                                 | Text       | Yes      |
| Reference   | Reference to another token (if not using direct value) | Text       | No\*     |
| Value       | Typography value with font properties                  | Typography | No\*     |
| Description | Optional explanation of the token's purpose            | Text       | No       |
| $extensions | Additional metadata for the token                      | Object     | No       |

\*Either Reference or Value must be provided

### Outputs

| Name  | Description                          | Type  |
| ----- | ------------------------------------ | ----- |
| Token | The complete typography design token | Token |

### How to Use It

1. Drag the Create Typography Design Token node into your graph.
2. Connect a name (like "typography.heading1") to the "Name" input.
3. Either connect a typography value from a Create Typography node to the "Value" input, or
4. Connect a reference string (like "{typography.base}") to the "Reference" input.
5. Optionally add a description and extensions as needed.

![Create Typography Design Token Example](screenshot-placeholder.png)

### Tips

* Use Value for direct typography definitions, or Reference to point to another typography token.
* Maintain consistent naming patterns for typography tokens across your design system.

### See Also

* **Create a Typography**: For creating typography values to use with this node.
* **Create Design Token**: For creating basic design tokens of other types.

### Use Cases

* **Text Styles Library**: Define a complete set of text styles for your application.
* **Responsive Typography**: Create typography tokens that adapt to different screen sizes.
* **Brand Implementation**: Ensure consistent typography across all brand applications.
