# Array Push

### What It Does
Adds a single item to the end of a list and gives you the updated list. It's perfect for growing collections like color palettes or spacing scales step-by-step.

### Inputs
| Name  | Description                     | Type  | Required |
|-------|---------------------------------|-------|----------|
| array | The list you want to add to     | List  | Yes      |
| item  | The single thing you want to add| Any   | Yes      |

### Outputs
| Name  | Description                     | Type  |
|-------|---------------------------------|-------|
| value | The new list with the item added| List  |

### How to Use It
1. Drag the Array Push into the editor.
2. Connect a list (like `[Red, Blue]`) to the "array" input.
3. Connect a single item (like `Green`) to the "item" input.
4. Run the graph—your output will be `[Red, Blue, Green]`.

![Array Push Example](screenshot-placeholder.png)

### Tips
- Match the item type to your list (e.g., don't add a number to a color list).
- Use this when building a list one item at a time.

### See Also
- **Array Concat**: For combining two lists.
- **Array Remove**: For taking items out of a list.

### Use Cases
- **Building a Color Palette**: Start with a base color list and add new shades (e.g., push `#33F` to `[#00F, #66F]`).
- **Spacing Scale**: Grow a spacing set by adding new values (e.g., push `16px` to `[4px, 8px]`).
- **Design Token Collection**: Add a new token (like a border style) to an existing token list. 