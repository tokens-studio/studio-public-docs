# Name tokens

### What It Does
The Name tokens node renames a collection of tokens sequentially by their index position. It automatically assigns names in multiples of 100 (100, 200, 300, etc.) based on each token's position in the array.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Tokens | The collection of tokens to rename | List | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Tokens | The renamed tokens with sequential names | List |

### How to Use It
1. Drag the Name tokens node into your graph.
2. Connect a list of tokens to the "Tokens" input.
3. The output will be the same tokens but with names set to "100", "200", "300", etc. based on their position.
4. Use these renamed tokens in other nodes that require named tokens.

![Name tokens Example](screenshot-placeholder.png)

### Tips
- This node overwrites any existing names in the tokens.
- The naming pattern follows multiples of 100, making it easy to insert tokens between existing ones later.

### See Also
- **Alphabetic**: For naming tokens with alphabetic sequences.
- **Numeric**: For more customizable numeric naming patterns.

### Use Cases
- **Automatic Naming**: Quickly name a set of tokens without manually entering each name.
- **Token Scale Creation**: Create evenly spaced naming for token scales (e.g., spacing or sizing scales).
- **Token Organization**: Establish a clear numerical ordering for tokens in a collection. 