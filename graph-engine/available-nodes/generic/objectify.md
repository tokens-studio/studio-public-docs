# Objectify

### What It Does
Combines multiple inputs of any type into a single object, where each input becomes a property in the resulting object. This allows you to group related values together into a structured format.

### Inputs
| Name     | Description                      | Type | Required |
|----------|----------------------------------|------|----------|
| (dynamic) | Properties to include in the object | Any | No |

### Outputs
| Name  | Description                           | Type   |
|-------|---------------------------------------|--------|
| value | Object containing all input properties | Object |

### How to Use It
1. Drag the Objectify node into your graph.
2. Right-click on the node and select "Add Input" to create new property inputs.
3. Name each input to define the property key in the resulting object.
4. Connect values to each input to set the corresponding property values.

![Objectify Example](screenshot-placeholder.png)

### Tips
- Property names in the resulting object match exactly the input names you define.
- Add as many inputs as needed to construct your object with all required properties.

### See Also
- **Object Path**: For extracting values from existing objects by path.
- **Object Merge**: For combining multiple existing objects.

### Use Cases
- **Token Structure**: Create structured design tokens that contain multiple related properties.
- **Component Configuration**: Build configuration objects for complex design components.
- **Data Organization**: Group related values into a logical structure for easier processing. 