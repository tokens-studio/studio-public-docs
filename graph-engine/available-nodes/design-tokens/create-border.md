# Create a Border

### What It Does
The Create a Border node generates a composite border value by combining color, width, and style properties. It's useful for creating consistent border definitions in your design system.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Color | The border color (e.g., "#000000" or "black") | Text | Yes |
| Width | The border thickness (e.g., "1px" or "0.25rem") | Text | Yes |
| Style | The border line style (e.g., "solid" or "dashed") | Text | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The composite border value | Border |

### How to Use It
1. Drag the Create a Border node into your graph.
2. Connect a color value (like "#E2E2E2") to the "Color" input.
3. Connect a width value (like "1px") to the "Width" input.
4. Connect a style value (like "solid") to the "Style" input.
5. The output provides a border value that can be used in border tokens.

![Create a Border Example](screenshot-placeholder.png)

### Tips
- Use standard CSS border styles: solid, dashed, dotted, etc.
- Width can use any CSS units (px, rem, em, etc.).

### See Also
- **Create Border Token**: For creating a complete border token with name and metadata.
- **Create Design Token**: For creating other types of design tokens.

### Use Cases
- **UI Component Borders**: Create consistent border styles for buttons, cards, and input fields.
- **Focus States**: Define border values for interactive element focus states.
- **Separator Lines**: Create subtle dividers between content sections. 