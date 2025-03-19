# Passthrough

### What It Does
Passes a value directly from input to output without modifying it. This is useful for reorganizing graph connections or making temporary connections during development.

### Inputs
| Name  | Description                  | Type | Required |
|-------|------------------------------|------|----------|
| value | The value to pass through    | Any  | Yes      |

### Outputs
| Name  | Description                  | Type |
|-------|------------------------------|------|
| value | The same value as the input  | Any  |

### How to Use It
1. Drag the Passthrough node into your graph.
2. Connect any value to the "value" input.
3. Connect the "value" output to any node that should receive the original value.
4. The node will simply pass the value through without changing it.

![Passthrough Example](screenshot-placeholder.png)

### Tips
- Use Passthrough nodes to clean up complicated graph layouts by redirecting connections.
- The node preserves the exact type of data passed through it, making it work with any value type.

### See Also
- **Note**: For adding comments to your graph without affecting data flow.
- **Objectify**: For combining multiple values into an object structure.

### Use Cases
- **Graph Organization**: Improve the readability of complex graphs by rerouting connections.
- **Debugging**: Insert between connections to create inspection points during development.
- **Interface Planning**: Use as placeholders when designing node interfaces before implementation. 