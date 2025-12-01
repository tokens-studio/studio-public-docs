# Group tokens

### What It Does
The Group tokens node adds a namespace to a token set, placing all tokens under a new group name. It creates a hierarchical structure by nesting the entire token set under the specified name.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Name | The name to use as the new group namespace | String | Yes |
| Token Set | The token set to be grouped under the new namespace | Object | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Token Set | The resulting token set with all tokens grouped under the new namespace | Object |

### How to Use It
1. Drag the Group tokens node into your graph.
2. Connect a token set to the "Token Set" input.
3. Set the "Name" input to the desired namespace (e.g., "colors").
4. The node will create a new token set with all tokens nested under the specified name.

![Group tokens Example](screenshot-placeholder.png)

### Tips
- This node is useful for organizing tokens into logical categories.
- You can create deeper nesting by using dot notation in the name (e.g., "theme.dark").
- Group multiple token sets separately and then merge them to create a comprehensive token structure.

### See Also
- **Ungroup tokens**: For removing a namespace from tokens.
- **Array to Set**: For converting a flat array of tokens to a hierarchical structure.

### Use Cases
- **Token Organization**: Organize tokens into logical categories like colors, typography, or spacing.
- **Theme Creation**: Create theme-specific token sets by grouping tokens under theme names.
- **Token Merging**: Prepare token sets for merging by grouping them under different namespaces. 