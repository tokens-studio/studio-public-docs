# Count

### What It Does

Calculates the number of items in an array. It simply returns the length of the input array, regardless of what type of items the array contains.

### Inputs

| Name  | Description                 | Type | Required |
| ----- | --------------------------- | ---- | -------- |
| value | The array to count items in | List | Yes      |

### Outputs

| Name  | Description                      | Type   |
| ----- | -------------------------------- | ------ |
| value | The number of items in the array | Number |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-02 at 19.23.14@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Count node into your graph.
2. Connect an array (like `[4, 5, 6, 7]`) to the "value" input.
3. Run the graph—with the example array, your output will be 4.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-02 at 19.21.56@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* Works with any type of array (numbers, strings, colors, mixed types, etc.).
* Empty arrays will return 0.
* This node counts only the top-level items; it doesn't count items in nested arrays.

### See Also

* [**Array Length**](https://documentation.tokens.studio/graph-engine/available-nodes/array/array-length): Alternative way to get the length of an array.
* [**Array Filter**](https://documentation.tokens.studio/graph-engine/available-nodes/array/array-filter): For counting only items that match specific criteria.
* [**Array Find**](https://documentation.tokens.studio/graph-engine/available-nodes/array/array-find): For locating specific items in an array.

### Use Cases

* **Validation**: Check if an array has any items or has a specific number of items.
* **Dynamic Layouts**: Adjust layouts based on the number of items to display.
* **Data Analysis**: Count the number of data points, colors, or other collection items.
* **Loop Control**: Use the count to determine how many iterations to perform.
