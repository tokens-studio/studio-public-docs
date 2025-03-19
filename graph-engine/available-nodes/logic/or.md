# Logical OR

### What It Does
Checks if at least one of the connected inputs is true and returns a single true/false result. This is useful for combining alternative conditions where any one being true is sufficient.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| inputs | Multiple values to check (can add as many as needed) | Any | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | True if any input is true/truthy, false otherwise | Yes/No |

### How to Use It
1. Drag the Logical OR node into your graph.
2. Click the "+" button to add as many input connections as you need.
3. Connect boolean values or conditions to each input.
4. Run the graph—your output will be true if at least one input is true.

![Logical OR Example](screenshot-placeholder.png)

### Tips
- Non-boolean values are converted to boolean: most values become true except falsy values (0, "", null, undefined).
- An OR node with no inputs will return false (similar to mathematical sum of an empty set).

### See Also
- **Logical AND**: For checking if all conditions are true.
- **NOT**: For inverting a boolean value.

### Use Cases
- **Fallback Logic**: Apply a style if either the primary or backup condition is met.
- **Multi-Criteria Matching**: Match an item if it satisfies any one of several possible criteria.
- **State Detection**: Detect when a component is in any one of several active states (hover OR focus OR active). 