# Create Design Token

### What It Does
The Create Design Token node generates a standard design token from basic inputs. It constructs a token object with name, type, value, and optional metadata that follows the Tokens Studio format. This node handles simple token types like color, dimension, fontFamily, and others.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Name | The name identifier for the token | String | Yes |
| Type | The token type (color, dimension, etc.) | String | Yes |
| Value | The token value | String | Yes |
| Description | Optional description of what the token represents | String | No |
| $extensions | Optional metadata for the token | Object | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Token | The complete design token object | Object |

### How to Use It
1. Drag the Create Design Token node into your graph.
2. Connect a string to the "Name" input to identify your token.
3. Select a token type from the available options (color, dimension, fontFamily, etc.).
4. Connect a string value appropriate for the chosen type.
5. Optionally add a description and any extension metadata.
6. The node will output a complete token object that follows the Tokens Studio format.

![Create Design Token Example](screenshot-placeholder.png)

### Tips
- Use this node for simpler token types like color, dimension, and fontFamily.
- For complex token types like typography, border, and boxShadow, use their dedicated creation nodes.
- Make sure your value format matches the expected format for the chosen token type.
- Use descriptive names that follow your design system's naming convention.

### See Also
- **Create Border Design Token**: For creating border tokens with multiple properties.
- **Create Typography Design Token**: For creating typography tokens with multiple properties.
- **Create Box Shadow Design Token**: For creating shadow tokens with multiple properties.
- **Flatten Token Sets**: For managing collections of tokens.

### Use Cases
- **Color Systems**: Create color tokens for your design system's palette.
- **Spacing System**: Define dimension tokens for your spacing scale.
- **Font Families**: Establish font family tokens for your typography system.
- **Motion Tokens**: Create duration tokens for animations and transitions. 