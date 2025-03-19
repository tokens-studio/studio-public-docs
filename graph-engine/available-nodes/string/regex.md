# Regex

### What It Does
Performs regular expression search and replace operations on text. It finds patterns in your input string and replaces them according to your specified replacement pattern.

### Inputs
| Name    | Description                                  | Type | Required |
|---------|----------------------------------------------|------|----------|
| input   | The text to process                          | Text | Yes      |
| match   | The regular expression pattern to find       | Text | No       |
| flags   | Regex flags (like "g" for global, "i" for case-insensitive) | Text | No |
| replace | The replacement pattern                      | Text | No       |

### Outputs
| Name  | Description                          | Type |
|-------|--------------------------------------|------|
| value | The text after pattern replacement   | Text |

### How to Use It
1. Drag the Regex node into your graph.
2. Connect the text you want to process to the "input" input.
3. Set the "match" value to the regular expression pattern you want to find (without the slashes).
4. Set any "flags" you need for the regex operation (e.g., "gi").
5. Define the "replace" pattern to substitute for matched text.

![Regex Example](screenshot-placeholder.png)

### Tips
- Don't include the slash delimiters in your match pattern - just the pattern itself.
- Use the "g" flag to replace all occurrences rather than just the first match.

### See Also
- **Replace**: For simple string replacement without regular expressions.
- **Normalize**: For standardizing text representation.

### Use Cases
- **Text Cleanup**: Remove or replace unwanted patterns or characters in text.
- **Format Conversion**: Transform text patterns from one format to another.
- **Data Extraction**: Isolate specific patterns from larger text blocks for token creation. 