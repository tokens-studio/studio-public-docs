# Deconstruct Float Curve

### What It Does

Breaks down a float curve into its fundamental components: segments (anchor points) and control points. This allows you to access and manipulate the individual parts of a curve.

### Inputs

| Name  | Description                    | Type        | Required |
| ----- | ------------------------------ | ----------- | -------- |
| curve | The float curve to deconstruct | Float Curve | Yes      |

### Outputs

| Name          | Description                                  | Type |
| ------------- | -------------------------------------------- | ---- |
| segments      | The anchor points that define the curve path | List |
| controlPoints | The handles that control the curve's shape   | List |

![Deconstruct Float Curve Example](<../../../.gitbook/assets/Screenshot 2025-04-09 at 8.13.34 PM.png>)

### How to Use It

1. Drag the Deconstruct Float Curve node into your graph.
2. Connect a float curve to the "curve" input.
3. Use the "segments" output to access the curve's anchor points.
4. Use the "controlPoints" output to access the curve's control handles.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-09 at 8.12.41 PM.png" alt=""><figcaption></figcaption></figure>

### Tips

* Segments are always one more than control point pairs in a properly constructed curve.
* Use this node when you need to modify individual points of an existing curve.

### See Also

* **Construct Float Curve**: For building a float curve from segments and control points.
* **Flip Float Curve**: For creating mirrored versions of a curve.

### Use Cases

* **Curve Analysis**: Examine the specific points that make up a curve.
* **Curve Manipulation**: Extract components to adjust them before reconstructing the curve.
* **Animation Control**: Fine-tune animation paths by accessing their component points.
