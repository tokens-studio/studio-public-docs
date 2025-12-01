# Tangent

### What It Does

The Tan node calculates the tangent of an angle value (in radians). Unlike sine and cosine which range from -1 to 1, tangent can produce values from negative infinity to positive infinity, creating more extreme oscillations.

### Inputs

| Name  | Description          | Type   | Required |
| ----- | -------------------- | ------ | -------- |
| Value | The angle in radians | Number | No       |

### Outputs

| Name  | Description                    | Type   |
| ----- | ------------------------------ | ------ |
| Value | The tangent of the input angle | Number |

![Tan Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 5.56.04 PM (2).png>)

### How to Use It

1. Drag the Tan node into your graph.
2. Connect a number to the "Value" input or use the default (0).
3. The output will be the tangent of the input angle.
4. Be aware that at certain values (like π/2, 3π/2, etc.), the output approaches infinity.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 5.56.45 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* The tangent function has vertical asymptotes at odd multiples of π/2 (±π/2, ±3π/2, etc.).
* For stable results, avoid angles too close to these asymptotes.
* The tangent is mathematically equivalent to sine/cosine.

### See Also

* **Sine**: For a bounded oscillating value between -1 and 1.
* **Cosine**: For another bounded oscillating value with a 90° phase shift from sine.

### Use Cases

* **Sharp Transitions**: Create dramatic, rapid changes in values.
* **Non-linear Mapping**: Transform linear inputs into non-linear outputs with steep changes.
* **Mathematical Modeling**: Implement specialized mathematical functions that require tangent calculations.
