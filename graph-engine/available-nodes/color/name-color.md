# Name Color

### What It Does

The Name Color node identifies the closest standard [CSS color name](https://www.w3schools.com/tags/ref_colornames.asp) for any color. It compares the input color to all named web colors and returns the name with the smallest perceptual difference.

### Inputs

| Name  | Description           | Type  | Required |
| ----- | --------------------- | ----- | -------- |
| Color | The color to identify | Color | Yes      |

### Outputs

| Name  | Description                                | Type   |
| ----- | ------------------------------------------ | ------ |
| Value | The name of the closest matching CSS color | String |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-21 at 17.43.05@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Name Color node into your graph.
2. Connect any color to the "Color" input (like `#E91BCB`).
3. The node will automatically find the closest CSS color name.
4. The output will be a string like "fuchsia", "mediumorchid", or "firebrick".

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-21 at 17.46.10@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* This node uses perceptual distance (Delta E) for matching to available CSS colors and provide accurate naming.
* CSS named colors are limited, so the result might not be an exact match.

### See Also

* [**String to Color**](string-to-color.md): For the reverse operation - converting color names to colors.
* [**Delta E**](delta-e.md): For calculating the difference between colors.

### Use Cases

* **Color Communication**: Convert exact color values to human-readable names for team discussions.
* **Design Documentation**: Generate descriptive color names for design specifications.
* **Data Visualization**: Simplify color data by grouping similar colors under standard names.
