# Flatten Alpha

### What It Does

The Flatten Alpha node blends a transparent foreground color with a solid background color to create a single opaque color. It calculates how the colors would appear when layered and removes transparency.

### Inputs

| Name       | Description                                         | Type  | Required |
| ---------- | --------------------------------------------------- | ----- | -------- |
| Foreground | The (potentially transparent) color to blend on top | Color | Yes      |
| Background | The solid background color to blend with            | Color | Yes      |

### Outputs

| Name  | Description                               | Type  |
| ----- | ----------------------------------------- | ----- |
| Value | The resulting opaque color after blending | Color |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 18.48.18@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Flatten Alpha node into your graph.
2. Connect a color with transparency to the "Foreground" input (e.g., `#FF000080`).
3. Connect a solid color to the "Background" input (e.g., `#000`).
4. The output will be an opaque color representing the visual appearance of the two blended colors (`#800000`).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 18.52.10@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* This node is useful for converting transparent colors to formats that don't support alpha channels.
* The background color should be fully opaque for accurate results.

### See Also

* [**Mix Colors**](mix.md): For blending colors with control over the mixing percentage.
* [**Color to String**](color-to-string.md): For converting the resulting color to a specific format.

### Use Cases

* **Format Conversion**: Convert RGBA colors to HEX for systems that don't support transparency.
* **Color Export**: Prepare colors with transparency for use in older design tools.
* **Visual Simulation**: Preview how transparent colors will appear against a specific background.
