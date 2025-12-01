# Object Merge

### What It Does

The Merge objects node combines multiple objects into a single object. It's perfect for consolidating data from different sources, with later objects in the array overriding properties from earlier ones in case of conflicts.

### Inputs

| Name         | Description                                                                                               | Type | Required |
| ------------ | --------------------------------------------------------------------------------------------------------- | ---- | -------- |
| Objects      | An array of objects to merge together                                                                     | List | No       |
| Concat Array | How arrays should be merged: "concat" (join arrays), "merge" (replace arrays), or "combine" (smart merge) | Text | No       |

### Outputs

| Name  | Description                 | Type |
| ----- | --------------------------- | ---- |
| Value | The resulting merged object | Any  |

![Merge objects Example](<../../../.gitbook/assets/Screenshot 2025-04-22 at 6.24.12 PM.png>)

### How to Use It

1. Drag the Merge objects node into your graph.
2. Connect an array of objects to the "Objects" input.
3. Select how you want arrays handled using the "Concat Array" input (defaults to "concat").
4. Run the graph to get a single merged object that combines all properties.

### Tips

* Objects later in the array will override properties from earlier objects when there are conflicts.
* Choose "concat" to join arrays, "merge" to replace them, or "combine" for a more intelligent merge.

### See Also

* **Objectify**: For creating an object from key-value pairs.
* **Object Property**: For accessing specific properties of an object.

### Use Cases

* **Token Combining**: Merge base tokens with theme-specific overrides to create a complete token set.
* **Configuration Building**: Combine default settings with user preferences to create a final configuration.
* **Data Aggregation**: Merge data objects from multiple sources into a single comprehensive object.
