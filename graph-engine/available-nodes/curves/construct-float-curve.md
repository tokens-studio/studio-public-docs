# Construct Float Curve

### What It Does
Creates a float curve by combining segment points and control points. It builds a mathematical curve representation that can be used for animations, transitions, or interpolations.

### Inputs
| Name          | Description                                  | Type     | Required |
|---------------|----------------------------------------------|----------|----------|
| segments      | The anchor points that define the curve path | List     | Yes      |
| controlPoints | The handles that control the curve's shape   | List     | Yes      |

### Outputs
| Name  | Description                            | Type        |
|-------|----------------------------------------|-------------|
| curve | The constructed float curve object     | Float Curve |

### How to Use It
1. Drag the Construct Float Curve node into your graph.
2. Connect an array of Vec2 points to the "segments" input (these are the anchor points).
3. Connect an array of Vec2 control point pairs to the "controlPoints" input.
4. The node outputs a complete float curve that can be used with other curve nodes.

![Construct Float Curve Example](screenshot-placeholder.png)

### Tips
- You must have exactly one more segment than control point pairs for a valid curve.
- Each segment is a [x,y] coordinate, and each control point is a pair of [x,y] coordinates.

### See Also
- **Deconstruct Float Curve**: For breaking a float curve into its component parts.
- **Sample Float Curve**: For evaluating a float curve at specific points.

### Use Cases
- **Custom Easing Functions**: Create precise animation timing curves for transitions.
- **Data Visualization**: Build custom curves for representing complex data relationships.
- **Path Generation**: Define smooth paths for design elements to follow. 