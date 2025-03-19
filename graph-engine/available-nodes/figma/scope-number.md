# Scope Number

### What It Does
The Scope Number node defines specific variable scopes for number tokens in Figma. It provides detailed control over where and how numeric variables can be used within Figma's interface.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Token | The design token to add scopes to | Token | Yes |
| Gap Between | Include gap between scope | Yes/No | No |
| Padding | Include padding scope | Yes/No | No |
| Corner Radius | Include corner radius scope | Yes/No | No |
| Font Weight | Include font weight scope | Yes/No | No |
| Font Size | Include font size scope | Yes/No | No |
| Line Height | Include line height scope | Yes/No | No |
| Letter Spacing | Include letter spacing scope | Yes/No | No |
| Paragraph Spacing | Include paragraph spacing scope | Yes/No | No |
| Paragraph Indent | Include paragraph indent scope | Yes/No | No |
| Layer Opacity | Include layer opacity scope | Yes/No | No |
| Effects | Include effects scope | Yes/No | No |
| Stroke | Include stroke scope | Yes/No | No |
| Text Content | Include text content scope | Yes/No | No |
| Width And Height | Include width and height scope | Yes/No | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Token | The token with number scopes applied | Token |

### How to Use It
1. Drag the Scope Number node into your graph.
2. Connect a number token to the "Token" input.
3. Check the boxes for contexts where the number should be available (e.g., Font Size, Corner Radius).
4. The output token will be available in Figma only for the selected contexts.

![Scope Number Example](screenshot-placeholder.png)

### Tips
- Group related numeric values with similar scopes to create a logical set of variables.
- Consider the purpose of each number to determine its appropriate scopes.

### See Also
- **Scope All**: For making a number available in all possible contexts.
- **Scope By Type**: For automatically assigning appropriate scopes based on token type.

### Use Cases
- **Spacing System**: Create spacing tokens that are only available for gap and padding properties.
- **Typography Scale**: Define text-specific numeric variables for font sizes and line heights.
- **Border System**: Create radius tokens that only appear in corner radius contexts. 