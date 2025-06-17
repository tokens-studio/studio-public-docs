---
hidden: true
---

# Creating a Sizing Scale

### What It Does

Creates a systematic sizing token system using linear progression. This multi-step workflow generates mathematically-related size values for component dimensions (width, height, containers), then converts them into properly named design tokens with hierarchical organization.

### Complete Workflow

This example demonstrates a 6-step process that transforms a single base size value into a complete token system:

1. **Base Size Setup**: Define the starting size value
2. **Linear Space Generation**: Create evenly distributed size values
3. **Token Creation**: Convert each size value into a named token
4. **Namespace Grouping**: Add hierarchical prefixes
5. **Set Conversion**: Format for token system output
6. **Final Export**: Output structured token set

### 1. Setting up the base size value

Creating a sizing scale starts with defining a base size unit that will determine the range of your sizing system. In this example, we'll use a 16px base unit to create a practical sizing scale for components.

**\[IMAGE: Screenshot showing Constant node configured for sizing]**

**Base Size Configuration:**

* Drag a **Constant** node (`Generic > Constant`) into your graph
* Set the **type** of the input to be **"Number"** from the dropdown
* Set your base size value to `16` (this will be your starting point)
* The node will output the numeric value ready for linear space generation

**Why Number Type**: Setting the input type to "Number" ensures the Linear Space node can perform proper mathematical calculations for even distribution.

### 2. Generating evenly distributed size values

Once we have the base size value, we need to generate a series of evenly distributed size values. The Linear Space node creates a mathematical progression from start to end with specified intervals.

**\[IMAGE: Screenshot showing Linear Space node connected to Constant node]**

**Linear Space Configuration:**

* Drag a **Linear Space** node into your graph
* Connect the output from your **Constant** node to the `start` input
* Configure the sizing parameters:
  * `start`: Connected from Constant (16)
  * `stop`: Set to `512` (your maximum size value for large components)
  * `length`: Set to `10` (number of size steps you want)
  * `precision`: Set to `0` (whole numbers only)
* The output will be an array of 10 evenly distributed size values: `[16, 71, 127, 182, 238, 293, 349, 404, 460, 512]`

**Linear Distribution**: The Linear Space node mathematically calculates even intervals between your start and stop values, ensuring consistent sizing relationships.

### 3. Token Creation (Array Map Subgraph)

We now have an array of size values that need to be converted into design tokens with systematic naming. The Array Map processes each size value through a subgraph that creates properly formatted tokens.

**\[IMAGE: Screenshot showing Array Map node connected to Linear Space]**

**Array Map Setup:**

* Drag an **Array Map** node and connect the Linear Space output to its `array` input
* Double-click the Array Map to enter the **Subgraph Explorer**

**\[IMAGE: Screenshot showing the complete Array Map subgraph for sizing tokens]**

**Subgraph Configuration:**

**Input Node:**

* Provides `value` (current size number), `index` (position), and `length` (total count)

**Stringify Node:**

* Connect `value` from Input node to `value` input
* Converts the numeric size value to string format (e.g., `16` becomes `"16"`)

**Numeric Scale Node:**

* Connect `index` from Input node to `index` input
* Set `multiplier` to `1` (sequential numbering)
* Leave `prefix` and `suffix` empty (just numbers: "1", "2", "3", etc.)

**Create Design Token Node:**

* Connect `name` from Numeric Scale output
* Connect `value` from Stringify output
* Set `type` to `"dimension"` (appropriate for size values)
* Leave `description` empty

**Output Node:**

* Connect from Create Design Token output to `value` input
* Set type to `"any"`

**Result**: Creates tokens with names like `1: "16"`, `2: "71"`, `3: "127"`, etc.

### 4. Adding namespace organization

The tokens from the Array Map need to be organized under a size namespace to create a hierarchical token structure.

**\[IMAGE: Screenshot showing Group Token Array node]**

**Group Token Array Configuration:**

* Drag a **Group Token Array** node into your graph
* Connect the `value` output from Array Map to the `tokens` input
* Set the `name` input to `"size"`

**What This Does**: Adds the "size." prefix to all token names, transforming `1`, `2`, `3`... into `size.1`, `size.2`, `size.3`...

### 5. Converting to token set format

**\[IMAGE: Screenshot showing Array of Tokens to Set node]**

**Token Set Conversion:**

* Drag an **Array of Tokens to Set** node
* Connect the tokens output from Group Token Array to the `tokens` input
* This formats the token array into the proper token set structure required for design systems

### 6. Final Output

**\[IMAGE: Screenshot showing Output node and final sizing table result]**

**Output Configuration:**

* Drag an **Output** node and connect the token set to it
* The final result displays your complete sizing scale

**Final Result:**\
The completed workflow generates a systematic sizing token set:

```json
{
  "size.1": "16",
  "size.2": "71", 
  "size.3": "127",
  "size.4": "182",
  "size.5": "238",
  "size.6": "293",
  "size.7": "349",
  "size.8": "404",
  "size.9": "460",
  "size.10": "512"
}
```

**\[IMAGE: Screenshot showing the complete final graph with all connections]**

**Usage Examples:**

* `size.1` (16px) - Small icons, avatars
* `size.3` (127px) - Medium buttons, input fields
* `size.6` (293px) - Card components, image containers
* `size.10` (512px) - Large hero sections, full-width components

**Customization**: You can adjust the `stop` value in Linear Space to create larger or smaller maximum sizes, or change the `length` to generate more or fewer size steps.
