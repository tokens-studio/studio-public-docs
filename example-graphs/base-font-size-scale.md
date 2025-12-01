---
hidden: true
---

# Creating a Font Size Scale

### What It Does

Creates a systematic font size scale using harmonic progression. This multi-step workflow generates mathematically-related font sizes that maintain visual harmony, then converts them into properly named design tokens with hierarchical organization.

### Complete Workflow

This example demonstrates a 6-step process that transforms a single base font size into a complete token system:

1. **Base Value Setup:** Define the starting font size
2. **Harmonic Series Generation:** Create mathematically related sizes
3. **Token Creation:** Convert each size into a named token
4. **Namespace Grouping:** Add hierarchical prefixes
5. **Set Conversion:** Format for token system output
6. **Final Export:** Output structured token set

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.00.21 PM.png" alt=""><figcaption><p>Base Font Scale</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.07.04 PM (1).png" alt=""><figcaption><p>Table Output</p></figcaption></figure>

{% stepper %}
{% step %}
### Setting up a base font size

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.34.44 PM.png" alt=""><figcaption></figcaption></figure>

Setting up a base font size which will be used as the foundation for generating the harmonic scale can be done in a number of ways using different nodes like [Constant](../graph-engine/available-nodes/generic/constant.md), [Input](../graph-engine/available-nodes/generic/input.md) etc. In this example, we will use Constant node as our starting point.

* Drag a Constant node (Generic > Constant) into your graph.
* Important: Set the type of the input to be "Number" from the dropdown.
* Set the value input to 16 (your base font size in pixels).
* The node will output the number value ready for mathematical operations.

> Why Number Type Matters: Setting the input type to "Number" ensures the Harmonic Series node can perform mathematical calculations on this value. Other types like "String" would prevent the harmonic progression from working correctly.


{% endstep %}

{% step %}
### Generating a harmonic font scale using the base size

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.37.42 PM.png" alt=""><figcaption></figcaption></figure>

Once we have the base font size as the output from our Constant node we want to generate a scale using the selected base size. To generate a harmonic font scale we will use a Harmonic Series node. This node takes a base value and generates a harmonic progression, the number of steps in the scale can be adjusted by adjusting the stepsUp and stepsDown inputs in the node.

* Drag a Harmonic Series node (Series > Harmonic Series) into your graph.
* Connect the output from your Constant node to the input named base in the Harmonic Series node.
* Configure the remaining inputs to create a balanced font scale:
* Set `stepsDown` to 0 (no smaller sizes below the base)
* Set `stepsUp` to 5 (generate 5 additional larger sizes above the base)
* Set `notes` to 5 (use 5 intervals within each octave for finer gradation)
* Set `ratio` to 2 (use a 2:1 ratio for harmonic progression)
* Set `precision` to 0 (round to whole numbers for pixel values)

The output will be an array of 6 font sizes: \[16, 18, 21, 24, 28, 32] from smallest to largest using harmonic relationships.

What This Creates: The harmonic series generates font sizes that are mathematically related, creating a visually pleasing progression. Each size maintains a musical relationship to the others, ensuring your typography scale feels balanced and harmonious.\
We now have a list of font sizes but these sizes are not yet in the design token format. In this example we want to convert these sizes into design tokens and also name our design tokens in a logical manner.
{% endstep %}

{% step %}
### Token Creation (Array Map Subgraph)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.40.43 PM.png" alt=""><figcaption></figcaption></figure>

To create design tokens and name the font sizes in our harmonic scale we will use Array Map node. Array map is an easy way to change or do certain actions on each item in our list. An array map will take each item in the list, do the changes that we specify inside the array map (subgraph) on each item of the list and give us a new list as an output.

* Drag an Array Map node (Array > Array Map) into your graph.
* Connect the array output of your Harmonic Series node to the array input of the Array Map node.
* To define what happens inside the Array Map, click on the "Subgraph Explorer" button.

Inside the Array map we see an input node and an output node.The input node inside the Array Map has the following outputs: value, index, length coming in from the Harmonic Series node. In the image below, we see a font size with value 32 at index 5 and the length of the array 6.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-10 at 5.29.58 PM.png" alt=""><figcaption></figcaption></figure>

**Converting the font size to string format**

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.38.07 PM.png" alt=""><figcaption><p>Stringify </p></figcaption></figure>

To create a design token we need to have the value as a string type, at this point the value that we have is a number type.

* To convert a number to string we will use a [Stringify](../graph-engine/available-nodes/string/stringify.md) node (String > Stringify).
* Drag the Stringify node into the subgraph and connect the value from the input node to the value input of the Stringify node.
* This will give us an output which is a string representation of the font size.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-10 at 5.37.06 PM.png" alt=""><figcaption></figcaption></figure>

#### Creating systematic token names

There are various ways that we can name the design token, for this example we will use the [Numeric Scale](../graph-engine/available-nodes/naming/numeric-scale.md) node.The Numeric Scale node allows us the option to have a multiplier, a prefix and a suffix.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.40.29 PM.png" alt=""><figcaption><p>Numeric Scale</p></figcaption></figure>

* Drag a Numeric Scale node (Naming > Numeric Scale) into your subgraph.
* Connect the index from the input node to the index input of the Numeric Scale node.
* Configure the naming pattern:
* Set `multiplier` to 1 (no scaling needed, just use sequential numbers)
* Set `prefix` to "size-" (text to add before the number)
* Leave `suffix` empty (no text needed after the number)

This will create names like "size-1", "size-2", etc. The Numeric Scale automatically adds 1 to the index before applying the multiplier, so index 0 becomes "size-1", index 1 becomes "size-2", and so on.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-10 at 5.41.18 PM.png" alt=""><figcaption></figcaption></figure>

Assembling the design token

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.45.47 PM.png" alt=""><figcaption></figcaption></figure>

Now we have the value and the name that we want to assign to our design token. To create a design token drag in the [Create Design Token](../graph-engine/available-nodes/design-tokens/create-design-token.md) node (Design Tokens > Create Design Token) into the subgraph.

* Connect the output from the Numeric Scale to the input called name in the Create Design Token node.
* Connect the output from the Stringify node to the input named value in the Create Design Token node.
* Set the type as "dimension" from the dropdown in the input panel on the right, this is to create a dimension design token appropriate for font sizes.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 2.58.31 PM.png" alt=""><figcaption><p>Inside the subgraph explorer</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.47.26 PM.png" alt=""><figcaption><p>Output</p></figcaption></figure>

Now we have created a Design Token. Connect the token output of the Create Design Token node to the Output node that was present in the Array Map.\
Important: Make sure the Output node type is set to "Any" to handle token objects properly. The output of the Array Map can be seen by clicking on the original graph.

**On the original graph:** right-click the Array Map node and click on "Force-Execute" to ensure that all the nodes inside the Array Map are executed on each item of our list from Harmonic Series node.\
The output of the Array Map will have a list of design tokens with the naming convention that we have created. Each font size from the Harmonic Series node has been transformed to a design token with the correct naming.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-10 at 5.52.31 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Adding a namespace to the Design Tokens names

We have the design tokens with the name as size-1, size-2, etc. For this example we want to add a namespace "font.size" to our design token names (font.size.size-1). To do this we will use the Group Token Array node, this node will let us add a namespace to an array of tokens.

* Drag the Group Token Array node (Design Tokens > Group Token Array) to the graph.
* In the input of the Group Token Array node, add "font.size" to the name input.
* Connect the value output from the Array Map to the tokens input of the Group Token Array.

The output will be a list of design tokens that has the naming convention of "font.size.size-1", "font.size.size-2", etc.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 4.40.07 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Creating a token set

At this point our design tokens are in a list or array. We need to convert the list to a token set before getting the final output.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 4.41.40 PM.png" alt=""><figcaption></figcaption></figure>

* To convert to a token set drag the Array of Tokens to Set node (Design Tokens > Array of Tokens to Set).
* Connect the tokens output from the Group Token Array to the tokens input of this node.
* This will convert our design tokens from an array to a token set.

```
{
  "font": {
    "size": {
      "size-1": {
        "value": "16",
        "type": "dimension"
      },
      "size-2": {
        "value": "18", 
        "type": "dimension"
      },
      "size-3": {
        "value": "21",
        "type": "dimension"
      }
      // ... continuing through size-6
    }
  }
}
```


{% endstep %}

{% step %}
### Final Output

To get the design tokens into the table format we need to connect it to the Output node.

Important: In the output node set the input in the right panel as "tokenSet".

* Connect the tokenSet output from the previous node to the input of the Output node.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 4.42.52 PM.png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Final Result

The graph is now complete and it will output the design tokens. Remember to click on the "Save" button to make sure that you do not lose your graph.To view the design tokens in table format, click on the "Table" button next to the "Save" button.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-10 at 6.13.21 PM.png" alt=""><figcaption></figcaption></figure>

We have a token set with harmonically-related font sizes generated from a single base size which creates a mathematically consistent typography scale. We can also now connect to the Tokens Studio for Figma plugin or the Companion by Tokens Studio plugin and use these design tokens in Figma.<br>
{% endstep %}
{% endstepper %}

<br>



<br>

<br>









