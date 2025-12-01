# Create Typography Design Token

### What It Does
The Create Typography Design Token node constructs a typography-type design token from provided inputs. It allows you to define typography properties such as font family, font weight, font size, line height, letter spacing, and more, generating a standardized token object that can be used in a design system.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Name | The name identifier for the token | String | Yes |
| Reference | A reference to another token (used when the token references another token) | String | No* |
| Value | Typography values defining font properties | Object | No* |
| Description | Optional description of what the token represents | String | No |
| $extensions | Optional metadata for the token | Object | No |

*Either Reference or Value must be provided

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Token | The complete design token object | Object |

### How to Use It
1. Drag the Create Typography Design Token node into your graph.
2. Connect a string to the "Name" input to identify your token.
3. Either:
   - Connect a typography values object to the "Value" input, or
   - Connect a reference string to the "Reference" input if this token references another token.
4. Optionally add a description and any extension metadata.
5. The node will output a complete typography token object that follows the Tokens Studio format.

![Create Typography Design Token Example](screenshot-placeholder.png)

### Tips
- Typography tokens typically include properties like fontFamily, fontSize, fontWeight, lineHeight, and letterSpacing.
- Use this node in combination with other token creation nodes to build a complete typography system.
- The "Reference" input allows you to create alias tokens that point to other typography tokens.
- Make sure your typography values follow the expected structure with all required properties.

### See Also
- **Create Color Design Token**: For creating color tokens.
- **Create Border Design Token**: For creating border tokens.
- **Create Box Shadow Design Token**: For creating shadow tokens.
- **Flatten Token Sets**: For managing collections of tokens.

### Use Cases
- **Text Styles**: Create consistent typography styles for different text elements.
- **Heading System**: Define a hierarchy of heading styles for your design system.
- **Body Text Variants**: Establish different body text styles for various contexts.
- **Special Text Elements**: Create typography tokens for captions, labels, and other specialized text components. 