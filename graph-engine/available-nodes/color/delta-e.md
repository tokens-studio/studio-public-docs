# Delta E

### What It Does

The Delta E node calculates the perceptual distance between two colors. It provides a numeric measurement of how different two colors appear to the human eye, using various industry-standard algorithms.

### Inputs

| Name      | Description                                                    | Type   | Required |
| --------- | -------------------------------------------------------------- | ------ | -------- |
| Color A   | First color for comparison                                     | Color  | No       |
| Color B   | Second color for comparison                                    | Color  | No       |
| Precision | Number of decimal places in the result                         | Number | No       |
| Algorithm | Color difference algorithm to use (76, CMC, 2000, Jz, ITP, OK) | String | No       |

### Outputs

| Name  | Description                               | Type   |
| ----- | ----------------------------------------- | ------ |
| Value | The calculated color difference (Delta E) | Number |

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 16.51.31@2x.png" alt=""><figcaption></figcaption></figure>

### How to Use It

1. Drag the Delta E node into your graph.
2. Connect two colors to "Color A" and "Color B" inputs.
3. Choose an algorithm (default is "2000", which is the industry-standard CIEDE2000).
4. Set the desired precision for the result (default is 4 decimal places).
5. The output value indicates how different the colors appear (higher values = more different).

<figure><img src="../../../.gitbook/assets/CleanShot 2025-03-20 at 16.56.59@2x.png" alt=""><figcaption></figcaption></figure>

### Tips

* Values below 1.0 are generally imperceptible to the human eye.
* Values between 1.0 and 2.0 are perceptible only with close observation.
* The CIEDE2000 (2000) algorithm is the most accurate for design work.

### See Also

* [**Distance**](distance.md): For calculating geometric distance between colors.
* [**Contrast**](contrast.md): For calculating contrast ratio between colors.
* [**Sort Colors By Distance**](sort-colors-by-distance.md): For sorting colors based on their differences.

### Use Cases

* **Color Matching**: Verify how close two colors appear to each other.
* **Palette Refinement**: Ensure colors in a palette are sufficiently distinct.
* **Accessibility Validation**: Check if color variations are perceptually different enough.
