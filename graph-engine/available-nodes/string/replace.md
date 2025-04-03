# Replace

### What It Does

Finds and replaces all occurrences of a search string with a replacement string. This is useful for removing, substituting, or modifying specific parts of text.

### Inputs

| Name    | Description                                        | Type   | Required |
| ------- | -------------------------------------------------- | ------ | -------- |
| string  | The original text to perform replacements on       | String | Yes      |
| search  | The text pattern to find and replace               | String | Yes      |
| replace | The new text to insert in place of the search text | String | No       |

### Outputs

| Name   | Description                               | Type   |
| ------ | ----------------------------------------- | ------ |
| string | The resulting text after all replacements | String |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 17.17.11@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Replace node into your graph.
2. Connect your source text to the "string" input (like `"Hello World"`).
3. Set the "search" input to the text you want to replace (like `"World"`).
4. Set the "replace" input to the replacement text (like `"Universe"`).
5. The output will be `"Hello Universe"`.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-04-03 at 17.18.44@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* To remove text entirely, leave the "replace" input empty or set it to an empty string.
* This node replaces all occurrences, not just the first match.
* This node is case sensitive.

### See Also

* [**Split**](split.md): For breaking text into parts based on a separator.
* [**Regex**:](regex.md) For more advanced pattern matching and replacement.

### Use Cases

* **Text Cleaning**: Remove unwanted characters or fix common typos in text.
* **Token Formatting**: Convert token references like `{spacing.sm}` to their actual values.
* **Content Variations**: Create different text versions by replacing key terms or phrases.
