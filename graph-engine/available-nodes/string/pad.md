# Pad

### What It Does

Adds characters to the beginning or end of a string until it reaches the desired length. This is useful for aligning text, creating fixed-width formats, or visual styling.

### Inputs

| Name      | Description                             | Type   | Required |
| --------- | --------------------------------------- | ------ | -------- |
| string    | The text to pad                         | String | Yes      |
| length    | The target length for the padded string | Number | Yes      |
| character | The character to pad with               | String | Yes      |
| position  | Where to add padding (start or end)     | String | No       |

### Outputs

| Name   | Description     | Type   |
| ------ | --------------- | ------ |
| string | The padded text | String |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 15.32.04@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Pad node into your graph.
2. Connect the text you want to pad to the "string" input. For e.g., `name`.
3. Set the desired "length" for the final string. For e.g., `10`.
4. Specify the "character" to use for padding (only the first character will be used).
5. Select the "position" to add padding (start or end).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 15.31.34@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* If your string is already longer than the specified length, it won't be truncated.
* Only the first character of the "character" input will be used for padding.

### See Also

* [**Case Convert**](case-convert.md): For changing text case format.
* [**Normalize**](normalize.md): For standardizing text representation.

### Use Cases

* **UI Display**: Create fixed-width elements for consistent visual alignment.
* **Code Formatting**: Format code identifiers with consistent spacing.
* **Data Export**: Prepare fixed-width fields for legacy systems or data exchange formats.
