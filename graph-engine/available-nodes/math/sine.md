# Sine

### What It Does

The Sine node calculates the sine of an angle value (in radians). It produces a smooth wave output that oscillates between -1 and 1, perfect for creating fluid animations and wave effects.

### Inputs

| Name  | Description          | Type   | Required |
| ----- | -------------------- | ------ | -------- |
| Value | The angle in radians | Number | No       |

### Outputs

| Name  | Description                 | Type   |
| ----- | --------------------------- | ------ |
| Value | The sine of the input angle | Number |

![Sine Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 5.27.24 PM.png>)

### How to Use It

1. Drag the Sine node into your graph.
2. Connect a number to the "Value" input or use the default (0).
3. The output will be the sine of the input angle, which ranges from -1 to 1.
4. Use this value for creating wave patterns and smooth oscillations.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 5.29.16 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* The output always ranges between -1 and 1.
* For smooth wave patterns, feed the Sine node with continuously increasing values.
* Common angles: sin(0) = 0, sin(π/2) = 1, sin(π) = 0, sin(3π/2) = -1.

### See Also

* **Cosine**: For calculating the cosine function (90° phase-shifted sine).
* **Tangent**: For calculating the tangent function.

### Use Cases

* **Smooth Animations**: Create natural, organic motion for UI elements.
* **Wave Effects**: Generate wave patterns for backgrounds, borders, or dynamic layouts.
* **Periodic Value Generation**: Create cycling values for recurring patterns in design tokens.
