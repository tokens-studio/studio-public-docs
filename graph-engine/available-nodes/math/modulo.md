# Modulo

### What It Does
The Modulo node calculates the remainder when dividing one number by another. It's useful for creating cycles, determining if a number is divisible by another, and implementing wrap-around behaviors.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| A | The dividend (number being divided) | Number | Yes |
| B | The divisor (number to divide by) | Number | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The remainder of A ÷ B | Number |

### How to Use It
1. Drag the Modulo node into your graph.
2. Connect your dividend to the "A" input.
3. Connect your divisor to the "B" input.
4. The output will be the remainder after division.

![Modulo Example](screenshot-placeholder.png)

### Tips
- The result is always less than the divisor (B).
- To check if a number is divisible by another, see if the modulo result is 0.
- Be careful when using negative numbers, as the result follows JavaScript's modulo behavior.

### See Also
- **Divide**: For getting the quotient of division.
- **Floor**: Often used with division to get integer division results.

### Use Cases
- **Cycling Patterns**: Create repeating patterns in design elements (every Nth item).
- **Alternating Styles**: Apply different styles based on element position (odd/even).
- **Constraint Ranges**: Keep values within a specific range by wrapping around. 