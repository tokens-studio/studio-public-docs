# Interpolation

### What It Does
Replaces placeholder variables in a string template with actual values. It allows you to create dynamic text by inserting variable content into a predefined template.

### Inputs
| Name     | Description                                         | Type | Required |
|----------|-----------------------------------------------------|------|----------|
| template | The string template with placeholders like {name}   | Text | Yes      |
| (dynamic)| Values to insert into the template                  | Any  | No       |

### Outputs
| Name  | Description                          | Type |
|-------|--------------------------------------|------|
| value | The final string with replaced values | Text |

### How to Use It
1. Drag the Interpolation node into your graph.
2. Connect your template string with placeholders in curly braces like "Hello, {name}!" to the "template" input.
3. Add custom inputs by right-clicking the node and adding inputs with names matching your placeholders.
4. Connect values to each named input to replace the corresponding placeholders.

![Interpolation Example](screenshot-placeholder.png)

### Tips
- Input names must exactly match the placeholder names in your template (without the curly braces).
- Placeholders that don't have a matching input will remain unchanged in the output.

### See Also
- **Join**: For combining multiple strings into one without using a template.
- **Replace**: For simpler find-and-replace text operations.

### Use Cases
- **Message Generation**: Create personalized messages by injecting names or other dynamic content.
- **URL Construction**: Build dynamic URLs by inserting variable parameters into a template.
- **Naming Patterns**: Generate consistent naming patterns for design tokens with variable components. 