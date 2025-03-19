# Alphanumeric Scale

### What It Does
The Alphanumeric Scale node generates combined letter-number identifiers (like A1, B2, C3) based on provided indices. It's useful for creating hierarchical naming systems with both alphabetic and numeric components.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Letter Index | Letter index (0 = A, 1 = B, etc.) | Number | Yes |
| Number Index | Number index (0 = 1, 1 = 2, etc.) | Number | Yes |
| Uppercase | Output letter in uppercase (true) or lowercase (false) | Boolean | No |
| Prefix | Optional text to add before the alphanumeric value | Text | No |
| Suffix | Optional text to add after the alphanumeric value | Text | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The generated alphanumeric value with optional prefix and suffix | Text |

### How to Use It
1. Drag the Alphanumeric Scale node into your graph.
2. Connect numbers to the "Letter Index" and "Number Index" inputs, or set them directly.
3. Configure optional inputs like case preference and prefix/suffix text.
4. The node will output a combined letter-number identifier (like "A1", "b2", etc.).

![Alphanumeric Scale Example](screenshot-placeholder.png)

### Tips
- Letter indices are clamped to the English alphabet range (0-25).
- Number indices automatically have 1 added (so index 0 produces "1").
- Combine with Count nodes to generate sequential alphanumeric identifiers.

### See Also
- **Alphabetic Scale**: For generating only alphabetic identifiers.
- **Numeric Scale**: For generating only numeric identifiers.
- **Name tokens**: For more complex token naming options.

### Use Cases
- **Grid Systems**: Create cell identifiers for design grids (A1, A2, B1, B2).
- **Variant Naming**: Organize component variants with hierarchical identifiers.
- **Section Numbering**: Create section identifiers for design documentation. 