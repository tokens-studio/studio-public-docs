# Exponential Decay

### What It Does

Generates a sequence of values that decrease according to the exponential decay formula P\*e^(-kx). This creates a curve that starts at an initial value and rapidly decreases at first, then tapers off gradually.

### Inputs

| Name         | Description                          | Type   | Required |
| ------------ | ------------------------------------ | ------ | -------- |
| initialValue | The starting value (P)               | Number | No       |
| length       | Number of values to generate         | Number | No       |
| decayRate    | The rate of decay (k)                | Number | No       |
| precision    | Number of decimal places to round to | Number | No       |

### Outputs

| Name   | Description                       | Type |
| ------ | --------------------------------- | ---- |
| values | The sequence of decreasing values | List |

![Exponential Decay Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 4.28.39 PM.png>)

### How to Use It

1. Drag the Exponential Decay node into your graph.
2. Set the "initialValue" (default is 100).
3. Set the "length" to specify how many values you want (default is 5).
4. Set the "decayRate" to control how quickly values decrease (default is 0.5).
5. Run the graph—with the default settings, your output will be \[100, 60.65, 36.79, 22.31, 13.53].

### Tips

* Higher decay rates cause values to decrease more rapidly.
* The decay is most dramatic at the beginning and gradually levels off.
* The values will never reach zero, but will get increasingly close as the sequence continues.

### See Also

* **Geometric Series**: For a similar sequence where each term is a constant multiple of the previous.
* **Arithmetic Series**: For sequences that decrease by a constant value.
* **Power Series**: For sequences based on powers of a number.

### Use Cases

* **Animation Easing**: Create natural-looking deceleration effects.
* **Fade Out Effects**: Generate opacity or volume values that gradually fade away.
* **Diminishing Returns**: Model scenarios where additional inputs yield increasingly smaller outputs.
* **Physical Systems**: Simulate natural decay processes like radioactive half-life or cooling.
