# Stringify

### What It Does

Converts any value type into a text string representation. This is useful for displaying non-text values or combining different data types into text format.

### Inputs

| Name  | Description                  | Type | Required |
| ----- | ---------------------------- | ---- | -------- |
| value | The value to convert to text | Any  | Yes      |

### Outputs

| Name  | Description                            | Type   |
| ----- | -------------------------------------- | ------ |
| value | The string representation of the input | String |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 17.32.28@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Stringify node into your graph.
2. Connect any value (number, boolean, object, etc.) to the "value" input.
3. The node will convert the input to its string representation.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 17.33.08@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* This node performs a simple conversion to string (equivalent to adding an empty string to a value).
* For more complex object serialization, consider using other tools to format the data.

### See Also

* [**Interpolation**](interpolation.md): For embedding values into a template string.
* [**Join Array**](join.md): For combining multiple strings into one.

### Use Cases

* **Display Formatting**: Convert numeric design tokens to string format for display.
* **Data Combination**: Convert values to strings before concatenating them with other text.
* **Type Conversion**: Ensure values are in string format before passing to string-only operations.
