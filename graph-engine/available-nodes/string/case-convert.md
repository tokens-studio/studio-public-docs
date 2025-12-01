# Case Convert

### What It Does

Transforms text between different case formats like camelCase, snake\_case, kebab-case, and PascalCase. It intelligently converts any string to your chosen case style.

### Inputs

| Name       | Description                            | Type   | Required |
| ---------- | -------------------------------------- | ------ | -------- |
| string     | The text to convert                    | String | Yes      |
| type       | The target case format                 | String | No       |
| delimiters | Characters to treat as word separators | String | No       |

### Outputs

| Name   | Description                       | Type   |
| ------ | --------------------------------- | ------ |
| string | The converted text in chosen case | String |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-24 at 10.59.38@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Case Convert node into your graph.
2. Connect the text you want to convert to the "string" input.
3. Select the desired case format from the "type" dropdown (camel, snake, kebab, or pascal).
4. Optionally specify custom delimiters if needed (default is "-\_.").

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-24 at 11.01.43@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* The node intelligently handles existing camelCase and PascalCase by adding spaces before capital letters.
* Custom delimiters let you control what characters are treated as word separators.

### See Also

* [**Uppercase**](uppercase.md): For converting text to ALL CAPS format.
* [**Lowercase**](lowercase.md): For converting text to all lowercase format.

### Use Cases

* **Design Token Naming**: Standardize variable names when generating design tokens for different platforms.
* **Code Generation**: Convert between naming conventions for different programming languages or frameworks.
* **API Integration**: Transform data fields between different naming conventions for API payloads.
