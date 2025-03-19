# Random

### What It Does
The Random node generates a random decimal number between 0 (inclusive) and 1 (exclusive). It's useful for creating variability, randomized designs, and simulating unpredictable behaviors.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| *None* | *This node has no inputs* | *N/A* | *N/A* |

### Outputs
| Name | Description | Type |
|------|-------------|------|
| Value | A random number between 0 and 1 | Number |

### How to Use It
1. Drag the Random node into your graph.
2. The node generates a random value when it's first created.
3. Connect the "Value" output to other nodes that need randomization.
4. Note that the value stays fixed after generation and doesn't change during execution.

![Random Example](screenshot-placeholder.png)

### Tips
- To get a random range other than 0-1, use math nodes to scale and shift the output.
- For values like 0-100, multiply the random value by 100.
- For ranges like 20-50, multiply by 30 (the range) and add 20 (the minimum).

### See Also
- **Range Mapping**: For mapping the 0-1 output to other ranges.
- **Multiply**: For scaling the random value.

### Use Cases
- **Variation in Design**: Add controlled randomness to spacing, sizing, or colors.
- **Testing Edge Cases**: Simulate different possible values during system testing.
- **Jitter Effects**: Add natural-looking variation to regular patterns or layouts. 