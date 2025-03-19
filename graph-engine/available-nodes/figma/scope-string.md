# Scope String

### What It Does
The Scope String node defines specific variable scopes for string tokens in Figma. It controls where and how text variables can be used within the Figma interface.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Token | The design token to add scopes to | Token | Yes |
| Font Family | Include font family scope | Yes/No | No |
| Font Style | Include font weight or style scope | Yes/No | No |
| Text Content | Include text content scope | Yes/No | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Token | The token with string scopes applied | Token |

### How to Use It
1. Drag the Scope String node into your graph.
2. Connect a string token to the "Token" input.
3. Check the boxes for contexts where the string should be available (e.g., Font Family, Text Content).
4. The output token will be available in Figma only for the selected contexts.

![Scope String Example](screenshot-placeholder.png)

### Tips
- Use Text Content scope for reusable text snippets or microcopy.
- Font Family and Font Style scopes are perfect for typography tokens.

### See Also
- **Scope All**: For making a string available in all possible contexts.
- **Scope By Type**: For automatically assigning appropriate scopes based on token type.

### Use Cases
- **Typography System**: Create font family variables that only appear in typography contexts.
- **Microcopy Library**: Define reusable text variables that appear as options for text content.
- **Brand Voice**: Maintain consistent language patterns by creating text variables with specific scopes. 