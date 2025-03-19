# Case Convert

### What It Does
Transforms text between different case formats like camelCase, snake_case, kebab-case, and PascalCase. It intelligently converts any string to your chosen case style.

### Inputs
| Name       | Description                                  | Type | Required |
|------------|----------------------------------------------|------|----------|
| string     | The text to convert                          | Text | Yes      |
| type       | The target case format                       | Text | No       |
| delimiters | Characters to treat as word separators       | Text | No       |

### Outputs
| Name   | Description                      | Type |
|--------|----------------------------------|------|
| string | The converted text in chosen case | Text |

### How to Use It
1. Drag the Case Convert node into your graph.
2. Connect the text you want to convert to the "string" input.
3. Select the desired case format from the "type" dropdown (camel, snake, kebab, or pascal).
4. Optionally specify custom delimiters if needed (default is "-_.").

![Case Convert Example](screenshot-placeholder.png)

### Tips
- The node intelligently handles existing camelCase and PascalCase by adding spaces before capital letters.
- Custom delimiters let you control what characters are treated as word separators.

### See Also
- **Uppercase**: For converting text to ALL CAPS format.
- **Lowercase**: For converting text to all lowercase format.

### Use Cases
- **Design Token Naming**: Standardize variable names when generating design tokens for different platforms.
- **Code Generation**: Convert between naming conventions for different programming languages or frameworks.
- **API Integration**: Transform data fields between different naming conventions for API payloads. 