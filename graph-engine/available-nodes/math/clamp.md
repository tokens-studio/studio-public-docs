# Clamp

### What It Does

Restricts a value to stay within a specified minimum and maximum range. If the value is below the minimum, it returns the minimum; if it's above the maximum, it returns the maximum; otherwise, it returns the original value.

### Inputs

| Name  | Description         | Type   | Required |
| ----- | ------------------- | ------ | -------- |
| value | The number to clamp | Number | No       |
| min   | The lower boundary  | Number | No       |
| max   | The upper boundary  | Number | No       |

### Outputs

| Name  | Description        | Type   |
| ----- | ------------------ | ------ |
| value | The clamped result | Number |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 19.04.12@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Clamp node into your graph.
2. Set "value" to the number you want to restrict (e.g., 12).
3. Set "min" to the lower bound (e.g., 5).
4. Set "max" to the upper bound (e.g., 10).
5. Run the graph—with the example values, your output will be 10 (since 12 exceeds the max).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 19.19.27@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* Make sure min is less than max, or the clamp will always return the min value.
* Clamp is useful for ensuring values stay within valid ranges before passing to other nodes.
* For colors and other non-numeric values, use specialized constraint nodes instead.

### See Also

* [**Range Mapping**](https://documentation.tokens.studio/graph-engine/available-nodes/math/range-mapping): For transforming values from one range to another.

### Use Cases

* **Boundary Enforcement**: Ensure values stay within acceptable limits.
* **Input Validation**: Sanitize user inputs to prevent extreme values.
* **Responsive Sizing**: Limit element sizes between minimum and maximum constraints.
* **Animation Control**: Prevent objects from moving outside defined areas.
