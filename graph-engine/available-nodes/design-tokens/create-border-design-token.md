# Create Border Design Token

### What It Does
The Create Border Design Token node constructs a border-type design token from provided inputs. It allows you to define border properties such as width, style, and color, and generates a standardized token object that can be used in a design system.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Name | The name identifier for the token | String | Yes |
| Reference | A reference to another token (used when the token references another token) | String | No* |
| Value | Array of border values defining width, style, and color | Array | No* |
| Description | Optional description of what the token represents | String | No |
| $extensions | Optional metadata for the token | Object | No |

*Either Reference or Value must be provided

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Token | The complete design token object | Object |

### How to Use It
1. Drag the Create Border Design Token node into your graph.
2. Connect a string to the "Name" input to identify your token.
3. Either:
   - Connect an array of border values to the "Value" input, or
   - Connect a reference string to the "Reference" input if this token references another token.
4. Optionally add a description and any extension metadata.
5. The node will output a complete border token object that follows the Tokens Studio format.

![Create Border Design Token Example](screenshot-placeholder.png)

### Tips
- Border tokens typically include properties like width, style (solid, dashed, etc.), and color.
- Use this node in combination with other token creation nodes to build a complete design token system.
- The "Reference" input allows you to create alias tokens that point to other tokens.
- Make sure your border values follow the expected structure with width, style, and color properties.

### See Also
- **Create Color Design Token**: For creating color tokens.
- **Create Typography Design Token**: For creating typography tokens.
- **Create Shadow Design Token**: For creating shadow tokens.
- **Flatten Token Sets**: For managing collections of tokens.

### Use Cases
- **Button Borders**: Create consistent border styles for different button states.
- **Input Field Styling**: Define border tokens for form fields in various states (default, focus, error).
- **Card Components**: Establish border styles for card components in a design system.
- **Dividers**: Create standardized border tokens for dividers and separators. 