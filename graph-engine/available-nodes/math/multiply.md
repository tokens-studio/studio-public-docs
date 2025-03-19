# Multiply

### What It Does
The Multiply node performs multiplication between two numbers. It's one of the fundamental math operations, useful for scaling values, calculating areas, and applying coefficients.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| A | The first number in the multiplication | Number | Yes |
| B | The second number in the multiplication | Number | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The product of A × B | Number |

### How to Use It
1. Drag the Multiply node into your graph.
2. Connect your first number to the "A" input.
3. Connect your second number to the "B" input.
4. The output will be the product of the two numbers.

![Multiply Example](screenshot-placeholder.png)

### Tips
- Multiplication is commutative, so the order of A and B doesn't matter.
- To scale a value by a percentage, multiply by the percentage divided by 100.
- Multiplying by 0 always gives 0, and multiplying by 1 leaves the value unchanged.

### See Also
- **Multiply (Variadic)**: For multiplying more than two numbers at once.
- **Divide**: For the inverse operation of multiplication.

### Use Cases
- **Scaling**: Adjust the size or intensity of values by a factor.
- **Area Calculations**: Calculate areas by multiplying width and height.
- **Percentage Adjustments**: Apply percentage-based modifications to values. 