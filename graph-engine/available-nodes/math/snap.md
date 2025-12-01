# Snap

### What It Does

The Snap node rounds a value to the nearest multiple of an increment, with an optional base offset. It's useful for creating grids, aligning values to specific intervals, and implementing design systems with consistent spacing.

### Inputs

| Name      | Description                                      | Type   | Required |
| --------- | ------------------------------------------------ | ------ | -------- |
| Value     | The value to snap                                | Number | No       |
| Increment | The step size to snap to                         | Number | No       |
| Base      | The starting point of the snap grid              | Number | No       |
| Method    | How to round values: "round", "floor", or "ceil" | Text   | No       |

### Outputs

| Name    | Description                                              | Type   |
| ------- | -------------------------------------------------------- | ------ |
| Snapped | The value snapped to the nearest increment from the base | Number |

![Snap Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 5.36.32 PM.png>)

### How to Use It

1. Drag the Snap node into your graph.
2. Connect a number to the "Value" input, or use the default (3).
3. Set your desired "Increment" (default 2) and "Base" (default 0).
4. Choose a "Method" for rounding: round (nearest), floor (lower), or ceil (higher).
5. The output will be the value snapped to your defined grid.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 5.34.13 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* Use "floor" to always snap down, "ceil" to always snap up, or "round" for nearest.
* For a grid starting at 0 with increment 8, values will snap to 0, 8, 16, 24, etc.
* With a base of 4 and increment 8, values will snap to 4, 12, 20, 28, etc.

### See Also

* **Round**: For simple rounding without custom increments.
* **Floor**: For always rounding down to the nearest integer.
* **Ceil**: For always rounding up to the nearest integer.

### Use Cases

* **Grid Alignment**: Snap positions to a grid for clean layouts.
* **Consistent Spacing**: Ensure spacing values follow your design system increments.
* **Value Quantization**: Convert continuous inputs to discrete steps (like music notes).
