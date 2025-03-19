# Array Find

### What It Does
Searches a list for the first item that matches your criteria. Unlike filter which returns all matches, this returns just the first matching item, its position, and whether anything was found.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| array | The list of items to search through | List | Yes |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The first matching item (if found) | Any |
| found | Whether a matching item was found | Yes/No |
| index | The position of the matching item (-1 if not found) | Number |

### How to Use It
1. Drag the Array Find node into your graph.
2. Connect your source list to the "array" input.
3. Double-click the node to open the inner search graph.
4. Create a condition in the inner graph that returns true for the item you want to find.
4. Run the graph—the outputs will contain the first matching item, if any.

![Array Find Example](screenshot-placeholder.png)

### Tips
- The inner graph has special inputs: "value" (current item), "index" (position), and "length" (total count).
- Always check the "found" output before using the "value" since it may be undefined if nothing matches.

### See Also
- **Array Filter**: For getting all matching items in a list.
- **Array Remove**: For removing items from a list.

### Use Cases
- **Token Lookup**: Find a specific color or spacing token by a property like its name or value.
- **Threshold Detection**: Find the first measurement in a scale that exceeds a certain value.
- **Default Selection**: Locate a fallback value in a list when a primary option isn't available. 