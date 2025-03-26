# Absolute

### What It Does

Returns the absolute (positive) value of a number by removing its sign. This is useful for calculating sizes, distances, or any values where direction doesn't matter.

### Inputs

| Name  | Description                             | Type   | Required |
| ----- | --------------------------------------- | ------ | -------- |
| input | The number to convert to absolute value | Number | Yes      |

### Outputs

| Name  | Description                                | Type   |
| ----- | ------------------------------------------ | ------ |
| value | The absolute (positive) value of the input | Number |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-26 at 16.27.30@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Absolute node into your graph.
2. Connect a number (like `-484.2`) to the "input".
3. Run the graph—your output will be `484`.
4. If you connect a positive number like `5`, it remains `5`.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-26 at 16.24.25@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* Use this node when you need to ensure a value is positive, such as for sizes or distances.
* Absolute values are useful for calculating differences without caring about which value is larger.

### See Also

* [**Clamp**](../../../node-examples/math/clamp.md): For setting minimum and maximum bounds on a value.
* [**Difference**](difference.md): For calculating the absolute difference between two numbers.

### Use Cases

* **Error Calculations**: Find how far a value is from a target without regard to direction.
* **Asset Sizing**: Ensure measurements stay positive even after calculations might result in negative values.
* **Responsive Design**: Calculate size differences between breakpoints regardless of which is larger.
