# String To Color

### What It Does

Converts a text representation of a color into a color object. This lets you transform hex codes, color names, or CSS color functions into usable color objects for your graph.

### Inputs

| Name  | Description                                                          | Type   | Required |
| ----- | -------------------------------------------------------------------- | ------ | -------- |
| color | The color string to convert (e.g., "#FF0000", "red", "rgb(255,0,0)") | String | Yes      |

### Outputs

| Name  | Description                        | Type  |
| ----- | ---------------------------------- | ----- |
| color | The parsed color as a color object | Color |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-21 at 17.45.19@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the String to Color node into your graph.
2. Connect a text string (like `"#3366CC"`, `"blue"`, or `"hsl(210, 100%, 50%)"`) to the "color" input.
3. Run the graph—your output will be a color object that can be used with other color nodes.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-21 at 17.49.51@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* The node accepts many formats: hex codes, color names, RGB, HSL, and more.
* Use this to convert color data from APIs, user inputs, or imported design tokens.

### See Also

* [**Color to String**](color-to-string.md): For converting color objects back to text representations.
* [**Create Color**](create.md): For building a color from individual channel values.

### Use Cases

* **Processing Input Data**: Convert color strings from imported data files or API responses.
* **Design Token Import**: Transform color tokens from text-based formats into usable color objects.
* **Dynamic Theming**: Parse color strings from configuration files or user preferences.
