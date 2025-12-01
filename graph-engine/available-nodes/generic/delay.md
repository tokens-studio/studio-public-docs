# Delay

### What It Does

The Delay node temporarily holds a value for a specific duration before passing it to the output. It's useful for creating timing effects or simulating processing time in your graph.

### Inputs

| Name  | Description                                                  | Type   | Required |
| ----- | ------------------------------------------------------------ | ------ | -------- |
| Value | The data you want to delay                                   | Any    | Yes      |
| Delay | How long to wait in milliseconds before outputting the value | Number | No       |

### Outputs

| Name  | Description                       | Type |
| ----- | --------------------------------- | ---- |
| Value | The delayed value (same as input) | Any  |

![Delay Example](<../../../.gitbook/assets/Screenshot 2025-04-22 at 6.21.30 PM.png>)

### How to Use It

1. Drag the Delay node into your graph.
2. Connect the value you want to delay to the "Value" input.
3. Set the "Delay" input (defaults to 1000ms if not specified).
4. When the node is triggered, it will wait for the specified delay and then output the value.

### Tips

* Use shorter delays (under 500ms) for subtle timing effects and longer delays for more noticeable pauses.
* The delay is measured in milliseconds (1000ms = 1 second).

### See Also

* **Passthrough**: For immediately passing values without delay.
* **Time**: For getting the current time or measuring durations.

### Use Cases

* **Animation Sequencing**: Delay different parts of a color or spacing animation to create staggered effects.
* **Simulated Loading**: Create realistic delays between state changes to mimic processing time.
* **Timed Updates**: Schedule token changes to happen after a certain period has elapsed.
