# Color Wheel

### What It Does

Generates a set of colors arranged in a color wheel pattern. Starting from a base hue, it creates a specified number of colors by rotating around the color wheel at consistent intervals, while maintaining the same saturation and lightness values.

### Inputs

| Name       | Description                                      | Type   | Required |
| ---------- | ------------------------------------------------ | ------ | -------- |
| baseHue    | The starting hue angle (0-360 degrees)           | Number | No       |
| angle      | The total angle to rotate around the color wheel | Number | No       |
| saturation | The saturation percentage for all colors (0-100) | Number | No       |
| lightness  | The lightness percentage for all colors (0-100)  | Number | No       |
| colors     | The number of colors to generate                 | Number | No       |

### Outputs

| Name  | Description                      | Type           |
| ----- | -------------------------------- | -------------- |
| value | An array of evenly spaced colors | List of Colors |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 11.19.51@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Color Wheel node into your graph.
2. Set the "baseHue" to your starting hue angle (default is 360/0, which is red).
3. Set the "angle" to determine how far around the wheel to go (default is 180 degrees).
4. Adjust "saturation" and "lightness" to control the vibrancy and brightness (defaults are 80%).
5. Set the "colors" value to determine how many colors to generate (default is 8).
6. Run the graph—your output will be an array of colors evenly distributed around the wheel.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 11.25.40@2x.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 11.45.27.gif" alt=""><figcaption></figcaption></figure>

### Tips

* For a full color wheel, set angle to 360 degrees.
* For complementary colors, use 2 colors with angle 180.
* For triadic colors, use 3 colors with angle 360.
* For analogous colors, use 3-5 colors with a smaller angle (30-60 degrees).

### See Also

* [**Range**](range.md): For creating a range between two specific colors.
* [**Scale Colors**](../preview/color-scale.md): For generating a graduated scale of a single color.
* [**Mix Colors**](mix.md): For blending between two specific colors.

### Use Cases

* **Color Harmonies**: Create complementary, triadic, or other color schemes.
* **Data Visualization**: Generate distinct colors for charts and graphs.
* **UI Theming**: Develop consistent color families for interface elements.
