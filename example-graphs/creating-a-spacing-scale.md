---
hidden: true
---

# Creating a Spacing Scale

What It Does

Creates a systematic spacing token system using linear progression. This multi-step workflow generates mathematically-related spacing values that maintain consistent visual rhythm, then converts them into properly named design tokens with hierarchical organization.

### Complete Workflow

This example demonstrates a 6-step process that transforms a single base spacing value into a complete token system:

1. **Base Spacing Setup**: Define the starting spacing value
2. **Linear Space Generation**: Create evenly distributed spacing values
3. **Token Creation**: Convert each spacing value into a named token
4. **Namespace Grouping**: Add hierarchical prefixes
5. **Set Conversion**: Format for token system output
6. **Final Export**: Output structured token set

### 1. Setting up the base spacing value

Creating a spacing scale starts with defining a base spacing unit that will determine the range of your spacing system. In this example, we'll use a 4px base unit to create a practical spacing scale.

**\[IMAGE: Screenshot showing Constant node configured for spacing]**

**Base Spacing Configuration:**

* Drag a **Constant** node (`Generic > Constant`) into your graph
* Set the **type** of the input to be **"Number"** from the dropdown
* Set your base spacing value to `4` (this will be your starting point)
* The node will output the numeric value ready for linear space generation

**Why Number Type**: Setting the input type to "Number" ensures the Linear Space node can perform proper mathematical calculations for even distribution.

### 2. Generating evenly distributed spacing values

Once we have the base spacing value, we need to generate a series of evenly distributed spacing values. The Linear Space node creates a mathematical progression from start to end with specified intervals.

**\[IMAGE: Screenshot showing Linear Space node connected to Constant node]**

**Linear Space Configuration:**

* Drag a **Linear Space** node into your graph
* Connect the output from your **Constant** node to the `start` input
* Configure the spacing parameters:
  * `start`: Connected from Constant (4)
  * `stop`: Set to `64` (your maximum spacing value)
  * `length`: Set to `8` (number of spacing steps you want)
  * `precision`: Set to `0` (whole numbers only)
* The output will be an array of 8 evenly distributed spacing values: `[4, 13, 21, 30, 38, 47, 55, 64]`

**Linear Distribution**: The Linear Space node mathematically calculates even intervals between your start and stop values, ensuring consistent spacing relationships.

### 3. Token Creation (Array Map Subgraph)

We now have an array of spacing values that need to be converted into design tokens with systematic naming. The Array Map processes each spacing value through a subgraph that creates properly formatted tokens.

**\[IMAGE: Screenshot showing Array Map node connected to Linear Space]**

**Array Map Setup:**

* Drag an **Array Map** node and connect the Linear Space output to its `array` input
* Double-click the Array Map to enter the **Subgraph Explorer**

**\[IMAGE: Screenshot showing the complete Array Map subgraph for spacing tokens]**

**Subgraph Configuration:**

**Input Node:**

* Provides `value` (current spacing number), `index` (position), and `length` (total count)

**Stringify Node:**

* Connect `value` from Input node to `value` input
* Converts the numeric spacing value to string format (e.g., `4` becomes `"4"`)

**Numeric Scale Node:**

* Connect `index` from Input node to `index` input
* Set `multiplier` to `1` (sequential numbering)
* Leave `prefix` and `suffix` empty (just numbers: "1", "2", "3", etc.)

**Create Design Token Node:**

* Connect `name` from Numeric Scale output
* Connect `value` from Stringify output
* Set `type` to `"dimension"` (appropriate for spacing values)
* Leave `description` empty

**Output Node:**

* Connect from Create Design Token output to `value` input
* Set type to `"any"`

**Result**: Creates tokens with names like `1: "4"`, `2: "13"`, `3: "21"`, etc.

### 4. Adding namespace organization

The tokens from the Array Map need to be organized under a spacing namespace to create a hierarchical token structure.

**\[IMAGE: Screenshot showing Group Token Array node]**

**Group Token Array Configuration:**

* Drag a **Group Token Array** node into your graph
* Connect the `value` output from Array Map to the `tokens` input
* Set the `name` input to `"spacing"`

**What This Does**: Adds the "spacing." prefix to all token names, transforming `1`, `2`, `3`... into `spacing.1`, `spacing.2`, `spacing.3`...

### 5. Converting to token set format

**\[IMAGE: Screenshot showing Array of Tokens to Set node]**

**Token Set Conversion:**

* Drag an **Array of Tokens to Set** node
* Connect the tokens output from Group Token Array to the `tokens` input
* This formats the token array into the proper token set structure required for design systems

### 6. Final Output

**\[IMAGE: Screenshot showing Output node and final spacing table result]**

**Output Configuration:**

* Drag an **Output** node and connect the token set to it
* The final result displays your complete spacing scale

**Final Result:**\
The completed workflow generates a systematic spacing token set:

```json
{
  "spacing.1": "4",
  "spacing.2": "13", 
  "spacing.3": "21",
  "spacing.4": "30",
  "spacing.5": "38",
  "spacing.6": "47",
  "spacing.7": "55",
  "spacing.8": "64"
}
```

**\[IMAGE: Screenshot showing the complete final graph with all connections]**

**Usage Examples:**

* `spacing.1` (4px) - Fine adjustments, button padding
* `spacing.3` (21px) - Component margins
* `spacing.5` (38px) - Section spacing
* `spacing.8` (64px) - Large layout gaps

**Customization**: You can adjust the `stop` value in Linear Space to create larger or smaller maximum spacing, or change the `length` to generate more or fewer spacing steps.
