# Group Token Array

### What It Does

The Group token array node adds a namespace prefix to all token names in an array, organizing them into a logical group. It prepends the specified name followed by a dot to each token's existing name.

### Inputs

| Name   | Description                             | Type | Required |
| ------ | --------------------------------------- | ---- | -------- |
| Name   | The namespace to add to all token names | Text | Yes      |
| Tokens | The array of tokens to group            | List | Yes      |

### Outputs

| Name   | Description                             | Type |
| ------ | --------------------------------------- | ---- |
| Tokens | The array of tokens with modified names | List |

### How to Use It

1. Drag the Group token array node into your graph.
2. Connect a string to the "Name" input (e.g., "colors" or "spacing").
3. Connect an array of tokens to the "Tokens" input.
4. The node will output the same tokens but with each name prefixed by the namespace and a dot.

![Group token array Example](arrays/screenshot-placeholder.png)

### Tips

* Use this to create hierarchical organization in your token sets.
* The grouping only affects the token names, not their values or other properties.

### See Also

* **Ungroup token array**: For removing namespace prefixes from token names.
* **Flatten Token Sets**: For flattening hierarchical token structures.

### Use Cases

* **Category Organization**: Group related tokens under categories like "color", "spacing", or "typography".
* **Component Tokens**: Organize component-specific tokens under component names.
* **Theme Variants**: Create theme-specific groupings like "dark" or "light".
