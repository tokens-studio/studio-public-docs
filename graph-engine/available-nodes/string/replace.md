# Replace

### What It Does
Finds and replaces all occurrences of a search string with a replacement string. This is useful for removing, substituting, or modifying specific parts of text.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| string | The original text to perform replacements on | Text | Yes |
| search | The text pattern to find and replace | Text | Yes |
| replace | The new text to insert in place of the search text | Text | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| string | The resulting text after all replacements | Text |

### How to Use It
1. Drag the Replace node into your graph.
2. Connect your source text to the "string" input (like `"Hello World"`).
3. Set the "search" input to the text you want to replace (like `"World"`).
4. Set the "replace" input to the replacement text (like `"Universe"`).
5. Run the graph—your output will be `"Hello Universe"`.

![Replace Example](screenshot-placeholder.png)

### Tips
- To remove text entirely, leave the "replace" input empty or set it to an empty string.
- This node replaces all occurrences, not just the first match.

### See Also
- **Split**: For breaking text into parts based on a separator.
- **Regex**: For more advanced pattern matching and replacement.

### Use Cases
- **Text Cleaning**: Remove unwanted characters or fix common typos in text.
- **Token Formatting**: Convert token references like `{spacing.sm}` to their actual values.
- **Content Variations**: Create different text versions by replacing key terms or phrases. 