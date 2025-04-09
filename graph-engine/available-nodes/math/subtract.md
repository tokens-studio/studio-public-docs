# Subtract

### What It Does

Subtracts one number from another, producing their difference. This basic math operation is useful for finding gaps between values or reducing numeric values.

### Inputs

| Name | Description                         | Type   | Required |
| ---- | ----------------------------------- | ------ | -------- |
| a    | The first number (minuend)          | Number | Yes      |
| b    | The number to subtract (subtrahend) | Number | Yes      |

### Outputs

| Name  | Description                | Type   |
| ----- | -------------------------- | ------ |
| value | The difference (a minus b) | Number |

![Subtract Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 5.45.31 PM.png>)

### How to Use It

1. Drag the Subtract node into your graph.
2. Connect a number (like `44`) to the "a" input.
3. Connect another number (like `33`) to the "b" input.
4. Run the graph—your output will be `10`.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 5.46.46 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* Remember that subtraction is not commutative: a - b is not the same as b - a.
* For absolute differences (regardless of which is larger), pair this with an Absolute node.

### See Also

* **Add**: For adding numbers together.
* **Multiply**: For multiplying numbers together.

### Use Cases

* **Spacing Adjustment**: Calculate the difference between container width and content width.
* **Relative Positioning**: Determine offsets from a base position in layouts.
* **Token Derivation**: Create derived tokens by subtracting values from a base token.
