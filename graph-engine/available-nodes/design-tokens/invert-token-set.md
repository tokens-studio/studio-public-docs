# Invert Token Set

### What It Does
The Invert Token Set node takes a collection of tokens and reverses their values while preserving their names. It's useful for creating inverse relationships like light/dark themes or flipping scales.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Tokens | The collection of tokens to invert | List | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Tokens | The inverted collection of tokens | List |

### How to Use It
1. Drag the Invert Token Set node into your graph.
2. Connect a list of tokens to the "Tokens" input.
3. The node will reverse the order of values while keeping the original token names.
4. Connect the output to other nodes that need to work with the inverted token set.

![Invert Token Set Example](screenshot-placeholder.png)

### Tips
- This is particularly useful for creating dark mode variants from light mode token sets.
- The token names remain the same, but their values are inverted in order.

### See Also
- **Flatten Token Sets**: For combining multiple token sets into a single flat array.
- **Group Tokens**: For organizing tokens into hierarchical structures.

### Use Cases
- **Light/Dark Theme Generation**: Invert color scales to create dark mode variants from light mode tokens.
- **Directional Variants**: Create RTL (right-to-left) spacing variants from LTR (left-to-right) tokens.
- **Alternate Scales**: Generate descending size scales from ascending ones while preserving semantic names. 