# Alphabetic Scale

### What It Does

The Alphabetic Scale node generates alphabetic characters (A through Z) based on an index value. It can output uppercase or lowercase letters and allows for optional prefix and suffix strings to be added to the result.

### Inputs

| Name      | Description                                     | Type    | Required |
| --------- | ----------------------------------------------- | ------- | -------- |
| Index     | Letter index (0 = A, 1 = B, etc.)               | Number  | Yes      |
| Uppercase | Output in uppercase (true) or lowercase (false) | Boolean | No       |
| Prefix    | Optional text to add before the letter          | String  | No       |
| Suffix    | Optional text to add after the letter           | String  | No       |

### Outputs

| Name  | Description                                                    | Type   |
| ----- | -------------------------------------------------------------- | ------ |
| Value | The generated alphabetic value with optional prefix and suffix | String |

### How to Use It

1. Drag the Alphabetic Scale node into your graph.
2. Connect a number to the "Index" input or set it directly (0-25 for A-Z).
3. Configure the optional inputs:
   * Set "Uppercase" to true for uppercase letters, false for lowercase.
   * Add a "Prefix" and/or "Suffix" if needed.
4. The node will output the corresponding letter with any prefix and suffix applied.

![Alphabetic Scale Example](../design-tokens/naming/screenshot-placeholder.png)

### Tips

* The index is clamped between 0-25 (the length of the English alphabet).
* Use this node in combination with Count or Range nodes to generate sequential lettering.
* For multi-letter naming (AA, AB, etc.), you may need to use multiple nodes or custom logic.

### See Also

* **Numeric**: For generating numeric sequences.
* **T-shirt Size**: For generating t-shirt size scales (XS, S, M, L, XL).
* **Name tokens**: For naming tokens with numeric increments.

### Use Cases

* **Variant Naming**: Create alphabetic variants for design elements (Option A, Option B, etc.).
* **Hierarchical Naming**: Generate alphabetic prefixes for hierarchical structures in designs.
* **Sequential Identification**: Create alphabetic identifiers for ordered elements in a design system.
