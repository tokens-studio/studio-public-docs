# Number

### What It Does

The Number node displays numeric values in a formatted way. It provides a visual preview of numbers with configurable precision.

### Inputs

| Name      | Description                          | Type   | Required |
| --------- | ------------------------------------ | ------ | -------- |
| Value     | The number to display                | Number | No       |
| Precision | The number of decimal places to show | Number | No       |

### Outputs

| Name         | Description                            | Type |
| ------------ | -------------------------------------- | ---- |
| _No outputs_ | This node is for preview purposes only | -    |

![Number Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 6.59.27 PM.png>)

### How to Use It

1. Drag the Number node into your graph.
2. Connect a numeric value to the "Value" input or use the default (12.27633).
3. Optionally set the "Precision" input to control decimal places (default is 2).
4. The node will display the formatted number for easy viewing (12.28).

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 6.59.43 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* Adjust the precision based on your needs—use higher values for more decimal places.
* Use this node to monitor calculated values at specific points in your graph.

### See Also

* [**Math Expression**](math-expression.md): For calculating mathematical expressions.
* [**Round**](../math/round.md): For rounding numbers to specific precisions.

### Use Cases

* **Value Monitoring**: Display important numeric values in your design system.
* **Calculation Verification**: Check intermediate or final calculation results.
* **Parameter Display**: Show current values of key parameters in your graph.
