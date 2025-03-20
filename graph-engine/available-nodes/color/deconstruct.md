# Deconstruct Color

### What It Does

Breaks a color down into its individual component values based on its color space. This gives you access to each channel (like red, green, blue in RGB) for separate manipulation.

### Inputs

| Name  | Description                             | Type  | Required |
| ----- | --------------------------------------- | ----- | -------- |
| color | The color to break down into components | Color | Yes      |

### Outputs

| Name  | Description                                                      | Type   |
| ----- | ---------------------------------------------------------------- | ------ |
| space | The color space of the input color                               | Text   |
| a     | The first channel value (e.g., red in RGB, hue in HSL)           | Number |
| b     | The second channel value (e.g., green in RGB, saturation in HSL) | Number |
| c     | The third channel value (e.g., blue in RGB, lightness in HSL)    | Number |
| alpha | The transparency value (0-1)                                     | Number |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 16.39.53@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Deconstruct Color node into your graph.
2. Connect a color (like `#4D6ADD`) to the "color" input.
3. Run the graph—each output will contain a separate component of the color.
4. Connect the individual channel outputs to other nodes for specific manipulations.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 16.47.03@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* The channel meanings (a, b, c) depend on the color's space (RGB, HSL, LAB, etc.).
* Use with Create Color to rebuild a color after modifying specific channels.

### See Also

* [**Create Color**](create.md): For rebuilding a color from individual channel values.
* [**Convert Color**](convert.md): For changing a color's space before deconstructing it.

### Use Cases

* **Channel Manipulation**: Extract the hue of a color to create variations with the same hue but different saturation/lightness.
* **Color Analysis**: Break down colors to understand their composition or for comparison.
* **Systematic Adjustments**: Modify just one aspect of a color (like saturation) while preserving other qualities.
