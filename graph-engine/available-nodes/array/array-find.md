# Array Find

What It Does

Creates a sub-graph that evaluates each item in an array, returning the first item where your condition evaluates to true. You define the matching condition in the inner graph using a custom combination of nodes.

### Inputs

| Name             | Description                                            | Type   | Required |
| ---------------- | ------------------------------------------------------ | ------ | -------- |
| array            | The array to search through                            | List   | Yes      |
| _Dynamic inputs_ | Any inputs you add to the inner graph will appear here | Varies | No       |

### Outputs

| Name  | Description                                                       | Type   |
| ----- | ----------------------------------------------------------------- | ------ |
| value | The first matching item found (undefined if none found)           | Any    |
| index | The position of the matching item in the array (-1 if none found) | Number |
| found | Whether a matching item was found                                 | Yes/No |

### Inner Graph Special Inputs

| Name   | Description                            | Type   |
| ------ | -------------------------------------- | ------ |
| value  | The current array item being evaluated | Any    |
| index  | The current position in the array      | Number |
| length | The total length of the array          | Number |

### Inner Graph Required Output

| Name    | Description                                     | Type   |
| ------- | ----------------------------------------------- | ------ |
| matches | Whether the current item matches your condition | Yes/No |

![Array Find Example](<../../../.gitbook/assets/Screenshot 2025-04-17 at 6.10.02 PM.png>)

### How to Use It

1. Drag the Array Find node into your graph.
2. Connect your array to the "array" input. In this example the input is a Geometric Series which outputs an array `[16, 24, 36, 54, 81, 122]`.
3. Click on the Subgraph Explorer button on the node to open and edit the inner graph.
4. In the inner graph, build your condition using the special "value" input. In this case a Compare node to check if the "value" is less than `50`.
5. Connect your condition's result to the "matches" input on the Output node.
6. Return to the main graph, where you can use the matched value, index, and found outputs. It outputs the first value that matches the condition. In this case the output is `16`.

<figure><img src="../../../.gitbook/assets/CleanShot 2025-05-05 at 19.17.41@2x.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/CleanShot 2025-05-05 at 19.17.55@2x.png" alt=""><figcaption><p>Subgraph explorer</p></figcaption></figure>

### Tips

* The inner graph runs once for each item in the array until a match is found.
* You can add your own inputs to the inner graph's Input node, which will appear as inputs on the main Array Find node.
* For complex comparisons, you can build any logic you need in the inner graph.

### See Also

* [**Array Filter**](array-filter.md): Similar to Array Find, but returns all matching items instead of just the first.
* [**Find First Match**](../search/find-first-match.md): For simple comparison-based searching (greater than, less than).
* [**Linear Search**](../search/linear-search.md): For exact-match searching.

### Use Cases

* **Finding Data by Complex Criteria**: Locate items based on multiple conditions or calculations.
* **Advanced Filtering**: When your matching logic requires multiple steps or operations.
* **Custom Search Algorithms**: Implement specialized search logic for your specific data structures.
