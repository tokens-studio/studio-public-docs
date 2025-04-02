# Add

### What It Does

Adds two numbers together to produce their sum. It's a basic math operation useful for combining numeric values like spacing tokens or opacity percentages.

### Inputs

| Name | Description              | Type   | Required |
| ---- | ------------------------ | ------ | -------- |
| a    | The first number to add  | Number | Yes      |
| b    | The second number to add | Number | Yes      |

### Outputs

| Name  | Description        | Type   |
| ----- | ------------------ | ------ |
| value | The sum of a and b | Number |

<div data-full-width="false"><figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 18.00.14@2x (1).png" alt=""><figcaption></figcaption></figure></div>

### How to Use It

1. Drag the Add node into your graph.
2. Connect a number (like 3) to the "a" input.
3. Connect another number (like `3`) to the "b" input.
4. Run the graph—your output will be 6.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-18 at 17.57.05@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* You can use the Add node with token references, like adding a base spacing value to an increment.
* For adding more than two numbers, chain multiple Add nodes together or use the Variadic Add node.

### See Also

* [**Subtract**](https://documentation.tokens.studio/graph-engine/available-nodes/math/subtract): For removing one number from another.
* [**Multiply**](https://documentation.tokens.studio/graph-engine/available-nodes/math/multiply): For multiplying numbers together.

### Use Cases

* **Spacing Calculations**: Add a base spacing unit (4px) to a multiplier to create consistent spacing increments in your design system.
* **Opacity Adjustments**: Add a percentage to a base opacity value to create a range of transparencies for different states.
* **Font Size Scaling**: Add a fixed increment to your base font size to create larger heading sizes.
