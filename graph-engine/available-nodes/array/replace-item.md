# Replace Item

### What It Does

Substitutes an item at a specific position in a list with a new item. The original list remains unchanged while a new list is created with the replacement.

### Inputs

| Name  | Description                           | Type   | Required |
| ----- | ------------------------------------- | ------ | -------- |
| array | The original list                     | List   | Yes      |
| item  | The new item to put into the list     | Any    | Yes      |
| index | The position to replace (starts at 0) | Number | Yes      |

### Outputs

| Name  | Description                     | Type |
| ----- | ------------------------------- | ---- |
| array | The list with the replaced item | List |

![Replace Item Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.31.17 PM.png>)

### How to Use It

1. Drag the Replace Item node into your graph.
2. Connect your list (like `[Red, Green, Blue]`) to the "array" input.
3. Connect the replacement item (like `Yellow`) to the "item" input.
4. Set the "index" value (e.g., 2 to replace the third item).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-05-07 at 18.53.47@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* Array indexes start at 0, so index 1 refers to the second item in the list.
* You can use negative indices to count from the end (-1 replaces the last item).

### See Also

* [**Inject Item**](inject-item.md): For inserting new items without replacing existing ones.
* [**Remove Item**](remove.md): For removing items from a list without replacements.

### Use Cases

* **Color Palette Refinement**: Replace a color in a palette with an improved version.
* **Token Update**: Swap out a specific design token in a collection with an updated value.
* **Content Revision**: Update specific items in a structured content list without changing the list structure.
