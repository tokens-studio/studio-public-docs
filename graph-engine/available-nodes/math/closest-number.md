# Closest Number

### What It Does

The Closest Number node finds the number in a list that's nearest to a specified target value. It's useful for finding the best match in a set of predefined values, such as snapping to the closest size in a design system.

### Inputs

| Name    | Description                             | Type   | Required |
| ------- | --------------------------------------- | ------ | -------- |
| Numbers | Array of numbers to search through      | List   | No       |
| Target  | Target number to find closest match for | Number | No       |

### Outputs

| Name       | Description                                           | Type   |
| ---------- | ----------------------------------------------------- | ------ |
| Index      | Index of the closest number in the array              | Number |
| Value      | The closest number found                              | Number |
| Difference | Absolute difference between target and closest number | Number |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 19.23.59@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Closest Number node into your graph.
2. Connect an array of numbers (like `[5, 10, 15, 25, 30]`) to the "Numbers" input, or use the default `[1, 2, 3]`.
3. Connect your target value (like `17`) to the "Target" input, or use the default `2`.
4. The outputs will show the closest value (`15`), its index in the array (`2`), and the difference from your target (`2`).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 19.40.39@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* The node returns the first occurrence when multiple numbers are equally close to the target.
* The input array must contain at least one number, or an error will be thrown.

### See Also

* [**Snap**](https://documentation.tokens.studio/graph-engine/available-nodes/math/snap): For rounding a value to specific increments.
* [**Linear Search**](https://documentation.tokens.studio/graph-engine/available-nodes/search/linear-search): For finding exact matches in an array.

### Use Cases

* **Design Token Selection**: Find the closest predefined spacing or font size in your design system.
* **Color Palettes**: Match a color to the nearest value in a restricted palette.
* **Responsive Breakpoints**: Determine which breakpoint is closest to the current viewport size.
