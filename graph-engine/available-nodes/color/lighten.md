# Lighten Color

### What It Does

Makes a color lighter by increasing its lightness by a specified amount. This is useful for creating tints of a base color or generating lighter variants for disabled states and background elements.

### Inputs

| Name  | Description                         | Type   | Required |
| ----- | ----------------------------------- | ------ | -------- |
| color | The color to lighten                | Color  | No       |
| value | How much to lighten the color (0-1) | Number | No       |

### Outputs

| Name  | Description         | Type  |
| ----- | ------------------- | ----- |
| value | The lightened color | Color |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 19.06.07@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Lighten Color node into your graph.
2. Connect a color (like `#1D1CEE`) to the "color" input.
3. Set a value between 0 and 1 (like `0.4`) to the "value" input.
4. Run the graph—your output will be a lighter version of the input color (`#77A0FF`).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 19.05.38@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* A value of 0 makes no change, while 1 produces white.
* Dark colors can be lightened more before losing their character than light colors.

### See Also

* [**Darken Color**](darken.md): For making colors darker instead of lighter.
* [**Mix Colors**](mix.md): For blending a color with white for more control.

### Use Cases

* **Disabled States**: Create lighter variants of interface elements to indicate disabled status.
* **Background Variations**: Generate lighter background colors that complement your main palette.
* **Tint Series**: Create a progression of increasingly lighter tints from a base brand color.
