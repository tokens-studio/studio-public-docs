# Pass Unit

### What It Does

The Pass unit node adds a unit to a value if it doesn't already have one. It ensures that string values representing measurements have the appropriate unit suffix.

### Inputs

| Name     | Description                                              | Type   | Required |
| -------- | -------------------------------------------------------- | ------ | -------- |
| Value    | The value to which a unit should be added                | String | Yes      |
| Fallback | The unit to add if no unit is present (defaults to "px") | String | No       |

### Outputs

| Name  | Description                  | Type   |
| ----- | ---------------------------- | ------ |
| Value | The value with unit attached | String |

### How to Use It

1. Drag the Pass unit node into your graph.
2. Connect a string value to the "Value" input.
3. Optionally, specify a fallback unit (defaults to "px").
4. The node checks if the value already has a unit.
5. If it does, the value is passed through unchanged.
6. If it doesn't, the fallback unit is appended to the value.

![Pass unit Example](screenshot-placeholder.png)

### Tips

* This node ensures consistent unit formatting in design tokens and CSS values.
* Useful for handling raw number inputs that should have specific units.
* The node won't add a unit to values that already contain one.

### See Also

* **Parse unit**: For extracting the number and unit from a value.
* **Parse Number**: For converting strings to numbers.
* **Stringify**: For converting any value to a string.

### Use Cases

* **Design Token Standardization**: Ensure all size values have appropriate units.
* **CSS Value Generation**: Add units to numeric values for CSS properties.
* **Unit Normalization**: Standardize values by ensuring they all have units.
* **Design System Implementation**: Enforce consistent unit usage across token values.
