# CSS Box

### What It Does
Creates CSS box model notation by combining four values (top, right, bottom, left) into a single space-separated string. This is the standard format used for CSS properties like margin, padding, and border-width.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| top | The top value | Number | No |
| right | The right value | Number | No |
| bottom | The bottom value | Number | No |
| left | The left value | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The combined CSS box value (e.g., "10 20 10 20") | Text |

### How to Use It
1. Drag the CSS Box node into your graph.
2. Set values for each side: "top" (e.g., 10), "right" (e.g., 20), "bottom" (e.g., 10), "left" (e.g., 20).
3. Run the graph—your output will be "10 20 10 20".
4. Use this output with CSS properties like margin, padding, or border-width.

![CSS Box Example](screenshot-placeholder.png)

### Tips
- This format follows the CSS standard: top, right, bottom, left (clockwise from the top).
- CSS has shorthand rules: if all four values are the same, you can use a single value.
- When using with CSS, you may need to add units (like "px" or "rem") after the generated string.

### See Also
- **CSS Function**: For creating other CSS functions like var(), calc(), etc.
- **CSS Accessible Clamp**: For generating responsive typography values.
- **String Join**: For combining strings with custom separators.

### Use Cases
- **Margins and Padding**: Define spacing around elements.
- **Border Width**: Set different border widths for each side of an element.
- **Position Offsets**: Define top, right, bottom, left values for positioned elements.
- **Design Tokens**: Create standardized spacing values for your design system. 