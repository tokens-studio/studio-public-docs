# Hierarchy Level

### What It Does

The Hierarchy Level node generates hierarchical level names (primary, secondary, tertiary, etc.) based on an index value. It provides semantic naming for items in a hierarchical structure.

### Inputs

| Name   | Description                                    | Type   | Required |
| ------ | ---------------------------------------------- | ------ | -------- |
| Index  | Level index (0 = primary, 1 = secondary, etc.) | Number | Yes      |
| Prefix | Optional text to add before the level name     | Text   | No       |
| Suffix | Optional text to add after the level name      | Text   | No       |

### Outputs

| Name  | Description                                                        | Type |
| ----- | ------------------------------------------------------------------ | ---- |
| Value | The generated hierarchy level name with optional prefix and suffix | Text |

### How to Use It

1. Drag the Hierarchy Level node into your graph.
2. Connect a number to the "Index" input or set it directly (0-9).
3. Optionally add prefix and suffix text if needed.
4. The node will output the corresponding hierarchy level name (like "primary", "secondary", "tertiary").

![Hierarchy Level Example](../design-tokens/naming/screenshot-placeholder.png)

### Tips

* The index is clamped between 0-9, supporting up to 10 hierarchy levels.
* Use these semantic names instead of numbers when creating hierarchical design systems.

### See Also

* **T-shirt Size**: For generating scale-based naming (XS, S, M, L, XL).
* **Numeric Scale**: For generating numeric sequences.
* **Name tokens**: For more complex token naming options.

### Use Cases

* **Button Hierarchy**: Define semantic levels for buttons (primary, secondary, tertiary).
* **Typography System**: Create named heading levels beyond h1-h6 nomenclature.
* **Color Importance**: Define a semantic color system based on hierarchical importance.
