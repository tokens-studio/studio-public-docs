# Create Box Shadow Design Token

### What It Does
The Create Box Shadow Design Token node creates a complete box shadow token by combining a name with box shadow value(s) or a reference. It's used to define standardized shadow effects in your design system.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Name | The token's identifier | Text | Yes |
| Reference | Reference to another token (if not using direct value) | Text | No* |
| Value | Array of box shadow values | List | No* |
| Description | Optional explanation of the token's purpose | Text | No |
| $extensions | Additional metadata for the token | Object | No |

*Either Reference or Value must be provided

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Token | The complete box shadow design token | Token |

### How to Use It
1. Drag the Create Box Shadow Design Token node into your graph.
2. Connect a name (like "shadow.card") to the "Name" input.
3. Either connect box shadow value(s) from Create Box Shadow nodes to the "Value" input, or
4. Connect a reference string (like "{shadow.base}") to the "Reference" input.
5. Optionally add a description and extensions as needed.

![Create Box Shadow Design Token Example](screenshot-placeholder.png)

### Tips
- Use Value for direct shadow definitions, or Reference to point to another shadow token.
- You can provide multiple box shadow values to create complex shadow effects.

### See Also
- **Create a Box Shadow**: For creating box shadow values to use with this node.
- **Create Design Token**: For creating basic design tokens of other types.

### Use Cases
- **Elevation System**: Define a systematic set of shadows for different UI elevations.
- **Component States**: Create shadow tokens for different interaction states (hover, active, etc.).
- **Dark/Light Modes**: Create shadow tokens that can be swapped for different themes. 