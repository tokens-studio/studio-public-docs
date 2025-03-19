# Lowercase

### What It Does
Converts all characters in a text string to lowercase (small letters). This helps create consistent text formatting or normalize user input for comparisons.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| value | The text to convert to lowercase | Text | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The converted lowercase text | Text |

### How to Use It
1. Drag the Lowercase node into your graph.
2. Connect a text string (like `"Hello World"`) to the "value" input.
3. Run the graph—your output will be `"hello world"`.
4. Special characters and numbers remain unchanged.

![Lowercase Example](screenshot-placeholder.png)

### Tips
- Lowercase is particularly useful for normalizing text for case-insensitive comparisons.
- It's often used for body text, URLs, and email addresses in design systems.

### See Also
- **Uppercase**: For converting text to all capital letters.
- **Case**: For more text casing options like title case or camel case.

### Use Cases
- **Text Normalization**: Standardize text from different sources for consistent display.
- **Search Terms**: Process search inputs for case-insensitive matching.
- **Design System Text**: Ensure consistent casing for body copy, captions, or labels. 