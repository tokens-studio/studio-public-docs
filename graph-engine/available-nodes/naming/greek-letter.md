# Greek Letter

### What It Does

The Greek Letter node generates Greek letter names (alpha through omega) based on an index value. It provides named steps for sequences where alphabetic or numeric scales aren't appropriate.

### Inputs

| Name   | Description                                  | Type   | Required |
| ------ | -------------------------------------------- | ------ | -------- |
| Index  | Letter index (0 = alpha, 1 = beta, etc.)     | Number | Yes      |
| Prefix | Optional text to add before the Greek letter | String | No       |
| Suffix | Optional text to add after the Greek letter  | String | No       |

### Outputs

| Name  | Description                                                | Type   |
| ----- | ---------------------------------------------------------- | ------ |
| Value | The generated Greek letter with optional prefix and suffix | String |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 22.28.28@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Greek Letter node into your graph.
2. Connect a number to the "Index" input or set it directly (0-23).
3. Optionally add prefix and suffix text if needed.
4. The node will output the corresponding Greek letter name (like "alpha", "beta", "gamma").

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 22.33.13@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* The index is clamped between 0-23 (the 24 Greek letters from alpha to omega).
* Greek letters are useful for representing variables or iteration sequences.

### See Also

* [**Alphabetic Scale**](alphabetic-scale.md): For generating Latin alphabet sequences.
* [**Numeric Scale**](numeric-scale.md): For generating numeric sequences.
* [**T-shirt Size**](t-shirt-size.md): For generating t-shirt size scales (XS, S, M, L, XL).

### Use Cases

* **Mathematical Variables**: Create named variables for mathematical expressions in design systems.
* **Phase Naming**: Label design phases using Greek letters (alpha phase, beta phase).
* **Alternative Sequences**: Provide a different naming convention when alphabetic or numeric scales are already in use.
