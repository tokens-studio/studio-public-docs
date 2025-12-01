# Ceiling

### What It Does

Rounds a number up to the nearest whole integer. This is useful for creating grid-based layouts, ensuring minimum sizes, or working with values that must be whole numbers.

### Inputs

| Name  | Description            | Type   | Required |
| ----- | ---------------------- | ------ | -------- |
| value | The number to round up | Number | Yes      |

### Outputs

| Name  | Description                                        | Type   |
| ----- | -------------------------------------------------- | ------ |
| value | The input number rounded up to the nearest integer | Number |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 18.57.50@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Ceil node into your graph.
2. Connect a number (like `12.65764`) to the "value" input.
3. Run the graph—your output will be `13`.
4. If the input is already a whole number (like `7`), the output remains the same (`7`).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 19.00.36@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* Use ceiling when you need to ensure a minimum number of items or size (like grid columns).
* Negative numbers are also rounded upward (e.g., -4.3 becomes -4).

### See Also

* [**Floor**](https://documentation.tokens.studio/graph-engine/available-nodes/math/floor): For rounding down to the nearest integer.
* [**Round**](https://documentation.tokens.studio/graph-engine/available-nodes/math/round): For rounding to the nearest integer (up or down).

### Use Cases

* **Grid Calculations**: Calculate how many grid cells are needed to fit content.
* **Pagination**: Determine the number of pages needed to display a set of items.
* **Sizing**: Ensure elements have at least a minimum pixel size, even with fractional calculations.
