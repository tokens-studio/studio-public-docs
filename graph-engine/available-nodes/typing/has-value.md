# Has Value

### What It Does
The Has Value node checks if a value is defined and outputs a boolean result. It evaluates whether the input is null or undefined, returning true if the value is missing and false if it exists.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Value | The value to check for existence | Any | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Result | True if the value is undefined or null, false otherwise | Boolean |

### How to Use It
1. Drag the Has Value node into your graph.
2. Connect any value to the "Value" input.
3. The node outputs true if the value is null or undefined.
4. Use the boolean output to control conditional logic in your graph.

![Has Value Example](screenshot-placeholder.png)

### Tips
- This node is useful for handling optional inputs gracefully.
- Combine with the If node to create fallback logic when values are missing.

### See Also
- **Assert defined**: For throwing an error when a value is undefined.
- **If**: For creating conditional branches based on the result.
- **Parse Number**: For checking if a value can be parsed as a number.

### Use Cases
- **Default Value Selection**: Check if a value exists before deciding to use a fallback.
- **Optional Parameter Handling**: Gracefully work with inputs that might not be provided.
- **Data Validation**: Verify the presence of data before processing it. 