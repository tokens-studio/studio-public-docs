# If

### What It Does
Makes a choice between two values based on a condition. When the condition is true, it returns the first value; otherwise, it returns the second value. This is essential for creating dynamic content or responsive behaviors.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| condition | The test that determines which value to use | Yes/No | Yes |
| a | The value to use when condition is true | Any | Yes |
| b | The value to use when condition is false | Any | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | Either value "a" or value "b" depending on the condition | Any |

### How to Use It
1. Drag the If node into your graph.
2. Connect a boolean (true/false) value to the "condition" input.
3. Connect your "true case" value to the "a" input.
4. Connect your "false case" value to the "b" input.
5. Run the graph—your output will be either value "a" or value "b".

![If Example](screenshot-placeholder.png)

### Tips
- You can use any type of values for the inputs, but both "a" and "b" should be compatible types.
- Chain multiple If nodes together to create more complex conditional logic.

### See Also
- **Switch**: For selecting from more than two options based on a value.
- **AND/OR**: For combining multiple conditions.

### Use Cases
- **Responsive Design**: Choose different spacing or typography based on screen size.
- **Theme Switching**: Select different colors depending on light/dark mode.
- **State Management**: Display different values based on UI state (hover, pressed, disabled). 