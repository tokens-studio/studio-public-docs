# Resolve tokens

### What It Does
The Resolve tokens node processes a set of design tokens, resolving any references between them into their actual values. It's essential for handling token aliasing and transforming abstract token definitions into concrete values.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Inputs | The primary set of tokens to resolve | List of Lists | Yes |
| Context | Additional tokens to use for reference resolution | List of Lists | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The resolved set of tokens with references replaced by actual values | List |

### How to Use It
1. Drag the Resolve tokens node into your graph.
2. Connect your primary tokens to the "Inputs" input.
3. Optionally, connect additional tokens as context for reference resolution to the "Context" input.
4. The output will be a flattened list of tokens with all references resolved to their actual values.

![Resolve tokens Example](screenshot-placeholder.png)

### Tips
- Context tokens are used for resolution but are excluded from the final output.
- The node maintains token structure but replaces reference values like `{color.primary}` with their actual values.

### See Also
- **Create Reference**: For creating references that can be resolved by this node.
- **Destruct Token**: For breaking down tokens into their individual components.

### Use Cases
- **Token Preprocessing**: Prepare tokens for export by resolving all internal references.
- **Reference Validation**: Verify that all token references can be successfully resolved.
- **Theme Generation**: Create complete theme sets with all abstract references resolved to concrete values. 