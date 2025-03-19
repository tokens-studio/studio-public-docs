# Token set to token array

### What It Does
The Token set to token array node converts a hierarchical token set structure into a flat array of individual tokens. It transforms nested token collections into a simple list that can be processed by nodes that expect token arrays.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Token Set | A hierarchical collection of design tokens | Object | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Tokens | A flat array of all tokens from the input set | List |

### How to Use It
1. Drag the Token set to token array node into your graph.
2. Connect a token set object to the "Token Set" input.
3. The node will flatten the hierarchical structure and output all tokens as a simple array.
4. Use the resulting token array with nodes that process individual tokens.

![Token set to token array Example](screenshot-placeholder.png)

### Tips
- This node preserves all token information including name, value, and type.
- The resulting array contains all tokens regardless of their original nesting level.
- Particularly useful when working with external token formats that use hierarchical structures.

### See Also
- **Array to Set**: For converting in the opposite direction.
- **Flatten**: For more advanced flattening operations on token arrays.

### Use Cases
- **Processing External Tokens**: Convert imported token sets into a format that can be processed by the graph.
- **Token Transformation**: Prepare tokens from a nested structure for batch operations.
- **Token Analysis**: Create a flat list of all tokens for inspection or validation. 