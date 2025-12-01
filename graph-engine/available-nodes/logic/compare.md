# Compare

### What It Does

Compares two values using one of several comparison operators. It evaluates the relationship between the inputs and outputs a boolean (true/false) result indicating whether the comparison is satisfied.

### Inputs

| Name     | Description                                       | Type | Required |
| -------- | ------------------------------------------------- | ---- | -------- |
| a        | The first value to compare                        | Any  | Yes      |
| b        | The second value to compare                       | Any  | Yes      |
| operator | The comparison operator to use (=, ≠, >, <, ≥, ≤) | Text | No       |

### Outputs

| Name  | Description                                                                         | Type   |
| ----- | ----------------------------------------------------------------------------------- | ------ |
| value | The result of the comparison (true if the comparison is satisfied, false otherwise) | Yes/No |

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 1.56.11 PM.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Compare node into your graph.
2. Connect the first value to compare to the "a" input.
3. Connect the second value to compare to the "b" input.
4. Select the desired operator from the dropdown (default is "equal").
5. Run the graph—the output will be true if the comparison is satisfied, false otherwise.



<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 2.50.47 PM.png" alt=""><figcaption></figcaption></figure>

### Supported Operators

| Operator              | Symbol | Description                             |
| --------------------- | ------ | --------------------------------------- |
| Equal                 | =      | True if a is equal to b                 |
| Not Equal             | ≠      | True if a is not equal to b             |
| Greater Than          | >      | True if a is greater than b             |
| Less Than             | <      | True if a is less than b                |
| Greater Than or Equal | ≥      | True if a is greater than or equal to b |
| Less Than or Equal    | ≤      | True if a is less than or equal to b    |

### Tips

* For string comparison, the operators follow JavaScript's string comparison rules.
* When comparing objects, "equal" means the same exact object, not just objects with the same properties.
* Mixing types in comparison may give unexpected results (e.g., comparing a string to a number).

### See Also

* **If**: For conditionally choosing between two values based on a boolean.
* **And**: For combining multiple conditions, requiring all to be true.
* **Or**: For combining multiple conditions, requiring at least one to be true.

### Use Cases

* **Conditional Logic**: Create branching logic based on value comparisons.
* **Data Validation**: Check if values meet specific criteria or thresholds.
* **Range Testing**: Verify if a value falls within or outside a specific range.
