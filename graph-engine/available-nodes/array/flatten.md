# Flatten

### What It Does

Flattens an array of arrays into a single level array, combining all nested elements into one unified list.

### Inputs

| Name  | Description                | Type | Required |
| ----- | -------------------------- | ---- | -------- |
| array | The nested list to flatten | List | Yes      |

### Outputs

| Name  | Description                  | Type |
| ----- | ---------------------------- | ---- |
| array | The resulting flattened list | List |

![Array flatten Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.14.52 PM.png>)

### How to Use It

1. Drag the Array flatten node into your graph.
2. Connect a nested list (like `[[1, 2], [3, 4]]`) to the "array" input.
3. The node will output a single flattened list (like `[1, 2, 3, 4]`).

### Tips

* This node only flattens one level deep, not recursively through all nested arrays.
* Make sure your input is actually an array of arrays, or the node will throw an error.

### See Also

* **Arrify**: For converting any value into an array format.
* **Concat**: For joining multiple arrays together end-to-end.

### Use Cases

* **Merging Token Groups**: Combine nested token groups into a flat structure for easier processing.
* **Simplifying Data Structures**: Convert complex nested lists of values into a simpler format for operations.
* **Processing Multi-dimensional Data**: Transform grid-based data into a linear sequence for sequential processing.
