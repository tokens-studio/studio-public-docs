# Base Font Size

### What It Does
Calculates an optimal base font size according to DIN 1450 standards, considering factors like viewing distance, screen properties, and visual acuity. This is useful for creating accessible typography that's properly sized for your specific use case.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| visualAcuity | Visual acuity factor (typical human vision is around 0.7) | Number | No |
| correctionFactor | Adjustment factor for calculation (default is 13) | Number | No |
| lightingCondition | Factor representing lighting conditions (bright to dim, 0-1) | Number | No |
| distance | Viewing distance in centimeters | Number | No |
| xHeightRatio | Ratio of x-height to font size in the typeface you're using | Number | No |
| ppi | Pixels per inch of the display | Number | No |
| pixelDensity | Pixel density factor (higher for retina/high DPI displays) | Number | No |
| precision | Decimal precision of the result | Number | No |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| value | The calculated base font size in pixels | Number |

### How to Use It
1. Drag the Base Font Size node into your graph.
2. Adjust the input values to match your specific scenario (device, viewing distance, etc.).
3. For most inputs, the default values work well for typical screen reading.
4. Connect the output to your typography system or use directly as a font size.

![Base Font Size Example](screenshot-placeholder.png)

### Tips
- The x-height ratio varies by font; common values are 0.5-0.55 for most typefaces.
- For accessibility, you may want to increase the result slightly beyond the calculated minimum.

### See Also
- **Font Size**: For directly setting font sizes or creating a scale.
- **Typography Style**: For creating complete text styles with multiple properties.

### Use Cases
- **Accessibility Compliance**: Ensure text meets readability standards for different devices.
- **Responsive Typography**: Calculate appropriate font sizes based on device characteristics.
- **Design Systems**: Create a scientifically-backed foundation for your typography scale. 