# Multiply (Variadic)

### What It Does
Multiplies two or more numbers together, calculating the product of all connected inputs. Unlike the basic Multiply node which has fixed inputs, this node can accept any number of values to multiply.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| inputs | The list of numbers to multiply together | List | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The product of all input values | Number |

### How to Use It
1. Drag the Multiply (Variadic) node into your graph.
2. Connect any number of numeric values to the "inputs" handle.
3. Each connected value will automatically be added to the inputs list.
4. Run the graph—the output will be the product of all connected values.
5. For example, with inputs [2, 3, 4], the output will be 24.

![Multiply (Variadic) Example](screenshot-placeholder.png)

### Tips
- You can keep connecting more inputs as needed—there's no limit.
- If no inputs are connected, the output will be 1 (the multiplicative identity).
- If any input is 0, the output will be 0 regardless of other values.

### See Also
- **Multiply**: The standard multiplication node with two fixed inputs.
- **Add Variadic**: For adding multiple values together.
- **Divide Variadic**: For dividing with multiple divisors.

### Use Cases
- **Scaling**: Apply multiple scaling factors to a base value.
- **Compound Effects**: Calculate the result of multiple percentage modifiers.
- **Dimensional Calculations**: Multiply length, width, and height for volume calculations.
- **Probability**: Calculate the combined probability of independent events. 