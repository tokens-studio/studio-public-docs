# Slice Array

### What It Does

Extracts a portion of a list to create a new list, based on start and end positions you specify. This lets you take a subset of items from any list.

### Inputs

| Name  | Description                                   | Type   | Required |
| ----- | --------------------------------------------- | ------ | -------- |
| array | The list to extract items from                | List   | Yes      |
| start | The beginning position (index starts at 0)    | Number | Yes      |
| end   | The end position (not included in the result) | Number | Yes      |

### Outputs

| Name  | Description                   | Type |
| ----- | ----------------------------- | ---- |
| value | The extracted portion of list | List |

![Slice Array Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.34.21 PM.png>)

### How to Use It

1. Drag the Slice Array node into your graph.
2. Connect your list (like `[Red, Orange, Yellow, Green, Blue]`) to the "array" input.
3. Set the "start" value (e.g., 1) and "end" value (e.g., 4).
4. The output will be the specified portion of the list (e.g., `[Orange, Yellow, Green]`).

### Tips

* The end index is not included in the result, so slice(1,4) returns items at positions 1, 2, and 3.
* You can use negative indices to count from the end of the list (-1 is the last item).

### See Also

* **Index Array**: For extracting a single item from a list.
* **Array Filter**: For selecting items based on a condition rather than position.

### Use Cases

* **Color Palette Segments**: Extract part of a color palette to use in a specific component.
* **Token Subsets**: Create smaller token collections from larger standardized sets.
* **Sequential Grouping**: Group related tokens together by extracting portions from a sequence.
