# Arrify

### What It Does

Takes any input value and ensures it is converted into an array format. It accepts various input types and transforms them into a uniform array structure.

### Inputs

| Name  | Description                                | Type | Required |
| ----- | ------------------------------------------ | ---- | -------- |
| items | The value(s) to be converted into an array | Any  | No       |

### Outputs

| Name  | Description                         | Type |
| ----- | ----------------------------------- | ---- |
| value | A properly formatted array of items | List |

![Arrify Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.11.40 PM.png>)

### How to Use It

1. Drag the Arrify node into your graph.
2. Connect any value or multiple values to the "items" input.
3. The node will output an array containing all input values.

### Tips

* This node is particularly useful when you need to standardize varied data formats into a consistent array structure.
* If you provide multiple inputs, they will all be included as elements in the resulting array.

### See Also

* **Array flatten**: For flattening nested arrays into a single level.
* **Concat**: For joining multiple arrays together end-to-end.

### Use Cases

* **Normalizing Data Structures**: Convert inconsistent data formats into standardized arrays for consistent processing.
* **Preparing Input for Array Operations**: Ensure values are in array format before applying array-specific nodes.
* **Creating Collections**: Gather multiple individual design tokens into a collection for batch processing.
