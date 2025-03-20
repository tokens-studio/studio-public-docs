# Parse Number

### What It Does

The Parse Number node converts a string representation of a number into an actual number value. If the conversion fails (resulting in NaN), the node throws an error.

### Inputs

| Name  | Description                       | Type   | Required |
| ----- | --------------------------------- | ------ | -------- |
| Value | The string to convert to a number | String | Yes      |

### Outputs

| Name  | Description                | Type   |
| ----- | -------------------------- | ------ |
| Value | The converted number value | Number |

### How to Use It

1. Drag the Parse Number node into your graph.
2. Connect a string value to the "Value" input.
3. The node attempts to convert the string to a number.
4. If successful, the number is output.
5. If the string cannot be parsed as a number, an error is thrown.

![Parse Number Example](screenshot-placeholder.png)

### Tips

* This node is stricter than JavaScript's built-in parsing as it throws an error on invalid input.
* Use this node when you need to ensure numerical operations will work correctly.
* Consider using a Try/Catch node to handle potential parsing errors gracefully.

### See Also

* **Parse unit**: For extracting both the number and unit from a value.
* **Pass unit**: For adding a unit to a number.
* **Number To String**: For converting in the opposite direction.

### Use Cases

* **User Input Validation**: Convert user-provided string inputs to numbers for calculations.
* **Data Cleaning**: Ensure values from external sources are proper numbers before processing.
* **Configuration Parameter Processing**: Convert string configuration values to numbers for use in calculations.
