---
hidden: true
---

# Length

### What It Does

The Vector2 Length node calculates the magnitude (absolute length) of a 2D vector. It's essential for measuring distances and normalizing vectors.

### Inputs

| Name   | Description              | Type    | Required |
| ------ | ------------------------ | ------- | -------- |
| Vector | The 2D vector to measure | Vector2 | Yes      |

### Outputs

| Name  | Description                          | Type   |
| ----- | ------------------------------------ | ------ |
| Value | The length (magnitude) of the vector | Number |

### How to Use It

1. Drag the Vector2 Length node into your graph.
2. Connect a 2D vector (like `[3, 4]`) to the "Vector" input.
3. The output will be the vector's length (for `[3, 4]`, the result would be `5`).
4. Use this value for distance measurements or to prepare for vector normalization.

![Vector2 Length Example](screenshot-placeholder.png)

### Tips

* The length is always positive, regardless of vector direction.
* For performance in comparisons, consider using the squared length (x² + y²) without the square root.

### See Also

* **Normalize**: For creating a unit vector (length of 1) from any vector.
* **Dot Product Vector2**: For calculating the scalar product of two vectors.

### Use Cases

* **Distance Calculation**: Measure the length of a displacement vector between two points.
* **Collision Detection**: Determine if objects are within a certain radius of each other.
* **Visual Scaling**: Size visual elements based on the magnitude of a vector property.
