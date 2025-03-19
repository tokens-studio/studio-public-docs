# CSS Function

### What It Does
Creates CSS function syntax by wrapping a value in one of the standard CSS functions (like var(), calc(), rgb(), etc.). This node formats the input value correctly according to CSS syntax rules.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| functionName | The CSS function to use | Text | Yes |
| value | The content to place inside the function | Text | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The complete CSS function with the value | Text |

### How to Use It
1. Drag the CSS Function node into your graph.
2. Select a function from the "functionName" dropdown (e.g., "var()").
3. Set the "value" you want inside the function (e.g., "--primary-color").
4. Run the graph—with the example values, your output will be "var(--primary-color)".

![CSS Function Example](screenshot-placeholder.png)

### Tips
- The function list includes all standard CSS functions from the MDN documentation.
- For functions that take multiple parameters, include them all in the value input with proper formatting.
- Remember to follow each function's syntax requirements for proper CSS output.

### See Also
- **CSS Accessible Clamp**: For generating responsive typography with clamp().
- **CSS Box**: For creating CSS box model properties.
- **String Interpolate**: For more complex string manipulation needs.

### Use Cases
- **CSS Variables**: Create var() references to design token variables.
- **Calculations**: Generate calc() expressions for dynamic layouts.
- **Colors**: Format RGB, HSL, or other color function notations.
- **Transforms**: Create transform functions like translate(), rotate(), scale(). 