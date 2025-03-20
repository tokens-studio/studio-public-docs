# Color To String

### What It Does

Converts a color object into a text representation in a specified format. This is useful when you need to output colors as hex codes, CSS color functions, or other text-based formats.

### Inputs

| Name  | Description                                | Type  | Required |
| ----- | ------------------------------------------ | ----- | -------- |
| color | The color to convert to text               | Color | No       |
| space | The format to output (hex, rgb, hsl, etc.) | Text  | No       |

### Outputs

| Name  | Description                | Type |
| ----- | -------------------------- | ---- |
| value | The color as a text string | Text |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 11.02.30@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Color to String node into your graph.
2. Drag the Input node and set the input type to "color". Set the input color (e.g. #2669F4)
3. Connect the output to the "color" input.
4. Choose an output format from the "space" dropdown (e.g., "hsl" for "hsl(225,0,0) format).
5. Run the graph—your output will be a text string like "#2669F4" or "hsl(220.49 90.351% 55.294%)".

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 11.05.12@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* The "hex" format is most common for web development and design tools.
* Other formats like "rgb" or "hsl" provide more readable information about the color's components.

### See Also

* [**String to Color**](string-to-color.md): For converting text color representations back into color objects.
* [**Deconstruct Color**](deconstruct.md): For breaking a color into its individual component values.

### Use Cases

* **CSS Output**: Generate color strings for use in CSS stylesheets or style objects.
* **Design Token Export**: Convert colors to string format for export to design token files.
* **Color Communication**: Create readable text versions of colors for documentation or sharing.
