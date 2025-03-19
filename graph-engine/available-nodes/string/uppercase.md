# Uppercase

### What It Does
Converts all characters in a text string to uppercase (capital letters). This is useful for creating consistent text formatting, headers, or emphasizing text.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| value | The text to convert to uppercase | Text | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The converted uppercase text | Text |

### How to Use It
1. Drag the Uppercase node into your graph.
2. Connect a text string (like `"Hello World"`) to the "value" input.
3. Run the graph—your output will be `"HELLO WORLD"`.
4. Special characters and numbers remain unchanged.

![Uppercase Example](screenshot-placeholder.png)

### Tips
- Uppercase is useful for creating consistent formatting regardless of input casing.
- Consider accessibility implications when using all caps, as it can be harder to read.

### See Also
- **Lowercase**: For converting text to all lowercase letters.
- **Case**: For more text casing options like title case or camel case.

### Use Cases
- **Button Labels**: Convert text to uppercase for button labels in a design system.
- **Headings & Titles**: Create standardized uppercase headings.
- **Acronyms**: Ensure acronyms and initialisms are consistently displayed in caps. 