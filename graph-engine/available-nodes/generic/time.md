# Time

### What It Does
Provides the current timestamp in milliseconds, updating automatically every second while the graph is running. It acts as a timer or clock source for time-based operations.

### Inputs
| Name | Description | Type | Required |
|------|-------------|------|----------|
| (none) | | | |

### Outputs
| Name  | Description                                      | Type   |
|-------|--------------------------------------------------|--------|
| value | Current time in milliseconds since Unix epoch    | Number |

### How to Use It
1. Drag the Time node into your graph.
2. Connect its "value" output to nodes that need time information.
3. The node will automatically update every second when the graph is running.
4. Use with math operations to create timing patterns or schedules.

![Time Example](screenshot-placeholder.png)

### Tips
- The time value is in milliseconds since January 1, 1970 (Unix epoch).
- Use the Math nodes to convert the timestamp to more usable formats like seconds or minutes.

### See Also
- **Delay**: For pausing execution for a specific duration.
- **Math Expression**: For converting timestamp to human-readable formats.

### Use Cases
- **Animation Timing**: Create time-based animations or transitions.
- **Scheduling**: Trigger events at specific times or intervals.
- **Timer Applications**: Build countdown timers or stopwatches for design prototyping. 