# Sort Array

### What It Does

Arranges items in a list in a specific order, either ascending or descending. It can sort by a specific property for complex objects, helping to organize collections.

### Inputs

| Name   | Description                                    | Type | Required |
| ------ | ---------------------------------------------- | ---- | -------- |
| array  | The list to be sorted                          | List | Yes      |
| order  | Direction of sort ("asc" or "desc")            | Text | No       |
| sortBy | Property name to sort by (for object elements) | Text | Yes      |

### Outputs

| Name  | Description     | Type |
| ----- | --------------- | ---- |
| value | The sorted list | List |

![Sort Array Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.37.35 PM.png>)

### How to Use It

1. Drag the Sort Array node into your graph.
2. Connect your list (like `[{name: "Blue", value: 5}, {name: "Red", value: 2}]`) to the "array" input.
3. Set "sortBy" to the property to sort on (e.g., "value").
4. Optionally change "order" to "desc" for descending order (default is "asc").

### Tips

* For simple lists (numbers or strings), use an empty string for the "sortBy" value.
* The sort is stable, meaning equal items maintain their relative order.

### See Also

* **Reverse Array**: For simply flipping the order of items without sorting.
* **Array Filter**: For selecting items rather than reordering them.

### Use Cases

* **Color Organization**: Sort colors by brightness, hue, or other properties.
* **Token Prioritization**: Arrange design tokens by their importance or frequency of use.
* **Size Sequencing**: Order spacing or sizing tokens from smallest to largest for consistent scales.
