# Color Swatch

### What It Does

The Color Swatch node displays a single color in a swatch format. It provides a visual preview of a color for design reference.

### Inputs

| Name  | Description                      | Type  | Required |
| ----- | -------------------------------- | ----- | -------- |
| Value | The color to display as a swatch | Color | Yes      |

### Outputs

| Name         | Description                            | Type |
| ------------ | -------------------------------------- | ---- |
| _No outputs_ | This node is for preview purposes only | -    |

![Color Swatch Example](<../../../.gitbook/assets/Screenshot 2025-04-08 at 7.01.39 PM.png>)

### How to Use It

1. Drag the Color Swatch node into your graph.
2. Connect a color value to the "Value" input.
3. The node will display the color as a swatch in the editor.
4. Use it to visually check the appearance of the color in your design system.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-08 at 7.04.28 PM (1).png" alt=""><figcaption></figcaption></figure>

### Tips

* Add multiple Color Swatch nodes to visualize different colors simultaneously.
* Use this node at key points in your graph to monitor color transformations.

### See Also

* [**Color Compare**](color-compare.md): For comparing two colors side-by-side.
* [**Color Scale**](color-scale.md): For visualizing a sequence of colors.

### Use Cases

* **Color Verification**: Visually confirm the exact appearance of generated colors.
* **Design System Reference**: Display brand colors or theme colors for reference.
* **Color Transformation**: Monitor color changes after operations like lightening, darkening, or mixing.
