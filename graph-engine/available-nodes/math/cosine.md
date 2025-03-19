# Cosine

### What It Does
The Cosine node calculates the cosine of an angle value (in radians). It's particularly useful for creating oscillating patterns, circular movements, and wave effects in design.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| Value | The angle in radians | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | The cosine of the input angle | Number |

### How to Use It
1. Drag the Cosine node into your graph.
2. Connect a number to the "Value" input or use the default (0).
3. The output will be the cosine of the input angle, which ranges from -1 to 1.
4. Use this value for creating cyclic patterns and oscillations.

![Cosine Example](screenshot-placeholder.png)

### Tips
- The output always ranges between -1 and 1.
- Use multiples of π (3.14159...) for common angles: 0 gives 1, π/2 gives 0, π gives -1.

### See Also
- **Sine**: For calculating the sine function (phase-shifted cosine).
- **Tangent**: For calculating the tangent function.

### Use Cases
- **Circular Motion**: Create circular or elliptical movements in animations.
- **Wave Patterns**: Generate smooth wave patterns for transitions or visual effects.
- **Color Cycling**: Create natural color oscillations by driving color components with cosine values. 