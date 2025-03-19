# Ungroup token array

### What It Does
The Ungroup token array node removes a namespace prefix from token names in an array. It filters tokens to only include those with the specified namespace and removes that prefix from their names.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Name | The namespace to remove from token names | Text | Yes |
| Tokens | The array of tokens to ungroup | List | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Tokens | The array of filtered tokens with simplified names | List |

### How to Use It
1. Drag the Ungroup token array node into your graph.
2. Connect a string to the "Name" input (e.g., "colors" or "spacing").
3. Connect an array of tokens to the "Tokens" input.
4. The node will filter tokens to only those starting with the given namespace, then remove that prefix from their names.

![Ungroup token array Example](screenshot-placeholder.png)

### Tips
- This node both filters and renames tokens in a single operation.
- Only tokens that start with the exact namespace followed by a dot will be included in the output.

### See Also
- **Group token array**: For adding namespace prefixes to token names.
- **Flatten Token Sets**: For flattening hierarchical token structures.

### Use Cases
- **Extract Subcategories**: Extract a specific category from a larger token collection.
- **Clean Up Imports**: Simplify token names from external sources by removing their namespaces.
- **Component Extraction**: Pull out component-specific tokens from a larger design system. 