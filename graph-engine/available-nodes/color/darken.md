# Darken Color

### What It Does

Makes a color darker by reducing its lightness by a specified amount. It's perfect for creating shades of a base color or generating darker variants for hover states and hierarchical elements.

### Inputs

| Name  | Description                        | Type   | Required |
| ----- | ---------------------------------- | ------ | -------- |
| color | The color to darken                | Color  | No       |
| value | How much to darken the color (0-1) | Number | No       |

### Outputs

| Name  | Description        | Type  |
| ----- | ------------------ | ----- |
| value | The darkened color | Color |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 16.02.26@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Darken Color node into your graph.
2. Connect a color (like `#5C9AFF`) to the "color" input.
3. Set a value between 0 and 1 (like `0.3`) to the "value" input.
4. Run the graph—your output will be a darker version of the input color (#1d59b8).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 16.05.25@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* A value of 0 makes no change, while 1 produces black.
* Use small increments (0.1-0.3) for subtle darkening effects in UI states.

### See Also

* [**Lighten Color**](lighten.md): For making colors lighter instead of darker.
* [**Mix Colors**](mix.md): For blending a color with black for more control.

### Use Cases

* **Button States**: Create darker variants of a button color for hover and active states.
* **Color Scales**: Generate a range of related dark shades from a base color.
* **Background Hierarchy**: Create darker backgrounds for elevated or nested UI elements.
