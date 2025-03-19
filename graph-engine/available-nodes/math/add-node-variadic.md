# Add Node (Variadic)

### What It Does
Adds two or more numbers together, summing up all the connected inputs. Unlike the basic Add node which has fixed inputs, this node can accept any number of values to add.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| inputs | The list of numbers to add together | List | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The sum of all input values | Number |

### How to Use It
1. Drag the Add Node (Variadic) into your graph.
2. Connect any number of numeric values to the "inputs" handle.
3. Each connected value will automatically be added to the inputs list.
4. Run the graph—the output will be the sum of all connected values.
5. For example, with inputs [5, 10, 15], the output will be 30.

![Add Node (Variadic) Example](screenshot-placeholder.png)

### Tips
- You can keep connecting more inputs as needed—there's no limit.
- If no inputs are connected, the output will be 0.
- This node is useful when you don't know in advance how many values you'll need to add.

### See Also
- **Add**: The standard addition node with two fixed inputs.
- **Sum**: For calculating the sum of values in an array.
- **Multiply Variadic**: For multiplying multiple values together.

### Use Cases
- **Flexible Calculations**: Perform addition with a variable number of inputs.
- **Dynamic Budgeting**: Add up expenses or income from multiple sources.
- **Cumulative Values**: Combine multiple metrics or measurements.
- **Configuration Sums**: Add together multiple customizable components of a value. 