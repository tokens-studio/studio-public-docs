# Inject Item

### What It Does

Adds a single item into a list at a specific position. Unlike push which adds to the end, this allows you to insert an item anywhere in the list.

### Inputs

| Name  | Description                        | Type   | Required |
| ----- | ---------------------------------- | ------ | -------- |
| array | The original list                  | List   | Yes      |
| item  | The item to insert into the list   | Any    | Yes      |
| index | The position to insert the item at | Number | Yes      |

### Outputs

| Name  | Description                      | Type |
| ----- | -------------------------------- | ---- |
| array | The list with the new item added | List |

![Inject Item Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.18.42 PM.png>)

### How to Use It

1. Drag the Inject Item node into your graph.
2. Connect your list (like `[Red, Blue]`) to the "array" input.
3. Connect the item to insert (like `Green`) to the "item" input.
4. Set the "index" value (e.g., 1 to insert between the first and second items).

### Tips

* Use index 0 to insert at the beginning of the list.
* You can use negative indexes to count from the end (-1 inserts before the last item).

### See Also

* **Array Push**: For adding items to the end of an array.
* **Replace**: For replacing existing items rather than inserting new ones.

### Use Cases

* **Color Palette Refinement**: Insert a transitional color between existing shades at a specific position.
* **Priority Insertion**: Add a new high-priority item in the middle of an existing sequence.
* **Layered Structure Design**: Insert elements between existing layers in a design structure.
