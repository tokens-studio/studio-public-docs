# Subtract Variadic

### What It Does

Performs sequential subtraction of multiple numbers, starting with the first value and subtracting each subsequent value. Unlike the basic Subtract node which has fixed inputs, this node can accept any number of values to subtract.

### Inputs

| Name   | Description                                  | Type | Required |
| ------ | -------------------------------------------- | ---- | -------- |
| inputs | The list of numbers to subtract sequentially | List | No       |

### Outputs

| Name  | Description                              | Type   |
| ----- | ---------------------------------------- | ------ |
| value | The result of the sequential subtraction | Number |

![Subtract (Variadic) Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 5.51.47 PM.png>)

### How to Use It

1. Drag the Subtract (Variadic) node into your graph.
2. Connect any number of numeric values to the "inputs" handle.
3. Each connected value will automatically be added to the inputs list.
4. Run the graph—the output will be the first value minus all subsequent values.
5. For example, with inputs \[3, 2, 1], the output will be 0 (3-2-1).



<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 5.52.02 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* You need at least one value for the node to work properly.
* Subtraction happens from left to right (first value minus second, result minus third, etc.).
* Order matters—the sequence \[10, 5, 2] gives a different result (3) than \[5, 10, 2] (-7).

### See Also

* **Subtract**: The standard subtraction node with two fixed inputs.
* **Add Variadic**: For adding multiple values together.
* **Difference**: For calculating the absolute difference between values.

### Use Cases

* **Budget Calculations**: Start with a total and subtract multiple expenses.
* **Time Intervals**: Calculate remaining time after subtracting multiple periods.
* **Inventory Management**: Track remaining stock after multiple withdrawals.
* **Resource Allocation**: Calculate remaining capacity after multiple allocations.
