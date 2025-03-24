# Interpolation

### What It Does

Replaces placeholder variables in a string template with actual values. It allows you to create dynamic text by inserting variable content into a predefined template.

### Inputs

| Name      | Description                                       | Type   | Required |
| --------- | ------------------------------------------------- | ------ | -------- |
| template  | The string template with placeholders like {name} | String | Yes      |
| (dynamic) | Values to insert into the template                | Any    | No       |

### Outputs

| Name  | Description                           | Type   |
| ----- | ------------------------------------- | ------ |
| value | The final string with replaced values | String |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-24 at 11.02.28@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Interpolation node into your graph.
2. Connect your template string with placeholders in curly braces like "color.{base}.500" to the "template" input. Here the placeholder is "base".
3. Add custom inputs by right-clicking the node and adding inputs with names matching your placeholders.&#x20;
4. Connect values to each named input to replace the corresponding placeholders. Like "red".
5. The output of the node is "color.red.500", the placeholder "base" is replaced by the named input "red".

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-24 at 11.08.54@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* Input names must exactly match the placeholder names in your template (without the curly braces).
* Placeholders that don't have a matching input will remain unchanged in the output.

### See Also

* [**Join**](join.md): For combining multiple strings into one without using a template.
* [**Replace**](replace.md): For simpler find-and-replace text operations.

### Use Cases

* **Message Generation**: Create personalized messages by injecting names or other dynamic content.
* **URL Construction**: Build dynamic URLs by inserting variable parameters into a template.
* **Naming Patterns**: Generate consistent naming patterns for design tokens with variable components.
