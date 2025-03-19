# Numeric Scale

### What It Does
The Numeric Scale node generates numeric values based on an index, with options to apply a multiplier and add prefix/suffix text. It's designed to create numerical sequences for systematic naming in design token collections.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Index | Base index number for the scale (starting at 0) | Number | Yes |
| Multiplier | Value to multiply the index by (e.g., 100 for scale of 100, 200, 300) | Number | No |
| Prefix | Optional text to add before the number | String | No |
| Suffix | Optional text to add after the number | String | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The generated numeric value with optional prefix and suffix | String |

### How to Use It
1. Drag the Numeric Scale node into your graph.
2. Connect a number to the "Index" input or set it directly.
3. Configure the optional inputs:
   - Set "Multiplier" to control the spacing between numbers (default is 1).
   - Add a "Prefix" and/or "Suffix" if needed.
4. The node will output a string with the calculated numeric value.

![Numeric Scale Example](screenshot-placeholder.png)

### Tips
- The node automatically adds 1 to the index before applying the multiplier, so index 0 produces the first number in the sequence.
- Use a multiplier of 100 to create standard design token scales (100, 200, 300).
- Connect this node to a Count node to generate a sequence of increasing numbers.

### See Also
- **Alphabetic Scale**: For generating alphabetic sequences.
- **T-shirt Size**: For generating t-shirt size scales (XS, S, M, L, XL).
- **Name tokens**: For automatically naming tokens with incremental numbers.

### Use Cases
- **Weight Scales**: Create systematic names for font weights or color intensity (100, 200, 300, etc.).
- **Spacing Systems**: Generate consistent spacing values at regular intervals.
- **Opacity Scales**: Create opacity values that follow a predictable pattern.
- **Elevation Systems**: Build systematic z-index or shadow elevation values. 