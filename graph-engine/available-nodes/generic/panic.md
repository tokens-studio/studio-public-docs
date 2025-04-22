# Panic

### What It Does

Throws an error and stops the graph execution when triggered by any truthy value. This acts as a deliberate fail-state for validation or testing purposes.

### Inputs

| Name    | Description                           | Type | Required |
| ------- | ------------------------------------- | ---- | -------- |
| trigger | Value that triggers the error if true | Any  | Yes      |

### Outputs

| Name   | Description | Type |
| ------ | ----------- | ---- |
| (none) |             |      |

### How to Use It

1. Drag the Panic node into your graph.
2. Connect the output of another node (like a condition or comparison) to the "trigger" input.
3. When the connected value is truthy (true, non-zero number, non-empty string, etc.), the graph will halt with an error.
4. Use this for input validation or to stop execution under specific conditions.

![Panic Example](<../../../.gitbook/assets/Screenshot 2025-04-22 at 6.31.06 PM.png>)

### Tips

* Combine with comparison nodes to create validation checks for your graph inputs.
* The error message will include the value that triggered the panic for easier debugging.

### See Also

* **If**: For conditional execution without stopping the graph.
* **Compare**: For comparing values before connecting to Panic.

### Use Cases

* **Input Validation**: Halt the graph if invalid design token values are detected.
* **Range Checking**: Ensure color values or numerical inputs stay within acceptable bounds.
* **Debug Testing**: Deliberately trigger errors during development to test error handling.
