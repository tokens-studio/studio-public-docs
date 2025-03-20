# T-Shirt Size

### What It Does

The T-Shirt Size node generates standardized t-shirt size naming conventions (XS, S, M, L, XL, etc.) based on index values. It supports different naming schemas (default, short, or long) and allows for customization with prefixes and suffixes.

### Inputs

| Name       | Description                                                       | Type   | Required |
| ---------- | ----------------------------------------------------------------- | ------ | -------- |
| Index      | Position relative to base index (negative for smaller sizes)      | Number | Yes      |
| Base Index | Index in the sequence that represents the base size (md/m/medium) | Number | No       |
| Schema     | Naming schema to use (default, short, or long)                    | String | No       |
| Prefix     | Optional text to add before the size                              | String | No       |
| Suffix     | Optional text to add after the size                               | String | No       |

### Outputs

| Name  | Description                                                      | Type   |
| ----- | ---------------------------------------------------------------- | ------ |
| Value | The generated t-shirt size value with optional prefix and suffix | String |

### How to Use It

1. Drag the T-Shirt Size node into your graph.
2. Connect a number to the "Index" input or set it directly.
3. Configure the optional inputs:
   * Set "Base Index" to determine which index corresponds to the medium size.
   * Choose a "Schema" (default: XS, S, M, L, XL; short: xs, s, m, l, xl; long: extra-small, small, medium, large, extra-large).
   * Add a "Prefix" and/or "Suffix" if needed.
4. The node will output the corresponding t-shirt size as a string.

![T-Shirt Size Example](../design-tokens/naming/screenshot-placeholder.png)

### Tips

* Use negative index values to get sizes smaller than the base size, and positive values for larger sizes.
* The node automatically clamps the result to the available sizes in the chosen schema.
* This naming convention is commonly used for spacing, component sizes, and breakpoints in design systems.

### See Also

* **Alphabetic Scale**: For generating alphabetic sequences.
* **Numeric Scale**: For generating numeric sequences.
* **Name tokens**: For automatically naming tokens with incremental numbers.

### Use Cases

* **Component Size Variants**: Create consistent size naming for component variants (button-s, button-m, button-l).
* **Spacing Systems**: Establish a familiar naming convention for spacing tokens.
* **Breakpoint Definitions**: Define standardized breakpoint names for responsive layouts.
* **Typography Scales**: Create readable size classifications for typography tokens.
