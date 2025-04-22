# Reverse Array

### What It Does

Flips the order of items in a list, making the last element first and the first element last. It creates a new reversed list without changing the original.

### Inputs

| Name  | Description             | Type | Required |
| ----- | ----------------------- | ---- | -------- |
| array | The list to be reversed | List | Yes      |

### Outputs

| Name  | Description       | Type |
| ----- | ----------------- | ---- |
| value | The reversed list | List |

![Reverse Array Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.32.42 PM.png>)

### How to Use It

1. Drag the Reverse Array node into your graph.
2. Connect your list (like `[Red, Green, Blue]`) to the "array" input.
3. The output will be the list in reverse order (e.g., `[Blue, Green, Red]`).

### Tips

* This node preserves the original list and outputs a new reversed copy.
* Useful for changing the visual priority or sequence of design elements.

### See Also

* **Sort**: For arranging items based on specific criteria rather than simply reversing them.
* **Array Filter**: For selectively including or excluding items from a list.

### Use Cases

* **Reversing Color Gradients**: Flip a color sequence to create an opposite gradient direction.
* **Priority Inversion**: Transform a list sorted by importance to focus on different priorities.
* **Visual Hierarchy Experimentation**: Test alternative arrangements of design elements by reversing their order.
