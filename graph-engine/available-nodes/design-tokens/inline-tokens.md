# Inline Tokens

### What It Does
The Inline Tokens node creates a set of design tokens that are stored directly within the graph. It allows you to define and reference tokens without requiring an external source.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Value | The collection of tokens to store inline | List | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Tokens | The stored collection of design tokens | List |

### How to Use It
1. Drag the Inline Tokens node into your graph.
2. Edit the node's properties to define your tokens directly in the graph editor.
3. The node will output the defined tokens for use in your design system.
4. Connect the output to other nodes that need to process or use these tokens.

![Inline Tokens Example](screenshot-placeholder.png)

### Tips
- Use this approach for small token sets or when you want to keep everything self-contained in your graph.
- The input is hidden in the UI as tokens are typically edited through the node's properties panel.

### See Also
- **External Token Set**: For importing tokens from external sources.
- **Create Design Token**: For creating individual tokens to add to a set.

### Use Cases
- **Quick Prototyping**: Create small token sets directly in your graph for rapid iteration.
- **Self-Contained Graphs**: Build portable graphs that don't rely on external files.
- **Default Values**: Define fallback token sets that can be overridden by external sources. 