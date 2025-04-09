# Round

### What It Does

The Round node adjusts a floating-point number to the nearest integer or to a specified precision. It's essential for cleaning up decimal values and ensuring consistent precision in your calculations.

### Inputs

| Name      | Description                         | Type   | Required |
| --------- | ----------------------------------- | ------ | -------- |
| Value     | The number you want to round        | Number | No       |
| Precision | How many decimal places to round to | Number | No       |

### Outputs

| Name  | Description        | Type   |
| ----- | ------------------ | ------ |
| Value | The rounded number | Number |

![Round Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 4.55.41 PM.png>)

### How to Use It

1. Drag the Round node into your graph.
2. Connect the number you want to round to the "Value" input.
3. Set the "Precision" input to specify how many decimal places to keep.
4. The output will be your number rounded to the specified precision.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 4.56.26 PM (1).png" alt=""><figcaption></figcaption></figure>

### Tips

* A precision of 0 (the default) rounds to the nearest whole number.
* Positive precision values round to that many decimal places (e.g., 2 gives 0.01 precision).
* To round to the nearest 10, 100, etc., use negative precision values (-1, -2, etc.).

### See Also

* **Floor**: For always rounding down to the nearest integer.
* **Ceil**: For always rounding up to the nearest integer.
* **Snap**: For rounding to specific increments beyond simple decimal places.

### Use Cases

* **Clean Decimal Display**: Ensure values display with a consistent number of decimal places.
* **Financial Calculations**: Round currency values to 2 decimal places.
* **Measurement Precision**: Control the precision of physical measurements in design systems.
