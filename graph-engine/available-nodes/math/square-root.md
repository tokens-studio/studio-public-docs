# Square Root

### What It Does

The Square Root node calculates the square root of a number - the value which, when multiplied by itself, equals the original number. It's essential for geometric calculations and creating non-linear scaling.

### Inputs

| Name     | Description                           | Type   | Required |
| -------- | ------------------------------------- | ------ | -------- |
| Radicand | The number to find the square root of | Number | Yes      |

### Outputs

| Name  | Description                         | Type   |
| ----- | ----------------------------------- | ------ |
| Value | The square root of the input number | Number |

![Square Root Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 5.40.54 PM.png>)

### How to Use It

1. Drag the Square Root node into your graph.
2. Connect a positive number to the "Radicand" input.
3. The output will be the square root of the input.
4. Use this for creating non-linear scales or calculating geometric properties.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 5.41.31 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* The input should be zero or positive for real number results.
* Using a negative input will result in NaN (Not a Number).
* Square root grows slower than linear functions, useful for compression effects.

### See Also

* **Pow**: For calculating powers, including the reverse operation of square root.
* **Abs**: For ensuring a value is positive before taking its square root.

### Use Cases

* **Non-linear Scaling**: Create spacing or sizing scales that grow more gradually.
* **Distance Calculations**: Compute distances in 2D or 3D space.
* **Visual Dampening**: Reduce extreme values while preserving smaller ones.
