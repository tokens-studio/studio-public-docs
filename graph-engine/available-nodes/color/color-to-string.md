# Color to String

### What It Does
Converts a color object into a text representation in a specified format. This is useful when you need to output colors as hex codes, CSS color functions, or other text-based formats.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| color | The color to convert to text | Color | No |
| space | The format to output (hex, rgb, hsl, etc.) | Text | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The color as a text string | Text |

### How to Use It
1. Drag the Color to String node into your graph.
2. Connect a color object to the "color" input.
3. Choose an output format from the "space" dropdown (e.g., "hex" for #RRGGBB format).
4. Run the graph—your output will be a text string like "#FF5500" or "rgb(255, 85, 0)".

![Color to String Example](screenshot-placeholder.png)

### Tips
- The "hex" format is most common for web development and design tools.
- Other formats like "rgb" or "hsl" provide more readable information about the color's components.

### See Also
- **String to Color**: For converting text color representations back into color objects.
- **Deconstruct Color**: For breaking a color into its individual component values.

### Use Cases
- **CSS Output**: Generate color strings for use in CSS stylesheets or style objects.
- **Design Token Export**: Convert colors to string format for export to design token files.
- **Color Communication**: Create readable text versions of colors for documentation or sharing. 