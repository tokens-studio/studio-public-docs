---
hidden: true
---

# Creating Multiple Color Scales

What It Does

Creates multiple systematic color palettes in a single workflow using parallel color scaling. This multi-step process generates complete color scales from different base colors, then converts each shade into properly named design tokens with hierarchical organization.

### Complete Workflow

This example demonstrates a 6-step process that transforms multiple base colors into a unified token system:

1. **Multiple Base Colors Setup**: Define starting colors for each palette
2. **Parallel Scale Generation**: Create algorithmically related shades for each color
3. **Individual Token Creation**: Convert each color into named tokens
4. **Array Combination**: Merge all color families into one array
5. **Set Conversion**: Format for token system output
6. **Final Export**: Output comprehensive token set

### 1. Setting up multiple base colors

Creating multiple color scales requires defining separate base colors that will each generate their own color family. In this example, we'll create both blue and red color scales using separate Constant nodes.

**Blue Base Color Setup:**

<figure><img src="../.gitbook/assets/Screenshot 2025-06-12 at 6.08.25 PM.png" alt=""><figcaption></figcaption></figure>

* Drag a **Constant** node (`Generic > Constant`) into your graph
* Set the **type** of the input to be **"Color"** from the dropdown
* Set your blue base color value (the color that all blue shades will be generated from)
* The node will output the blue color value ready for scale generation

**Red Base Color Setup:**

<figure><img src="../.gitbook/assets/Screenshot 2025-06-12 at 6.07.48 PM.png" alt=""><figcaption></figcaption></figure>

* Drag a second **Constant** node (`Generic > Constant`) into your graph
* Set the **type** of the input to be **"Color"** from the dropdown
* Set your red base color value (the color that all red shades will be generated from)
* The node will output the red color value ready for scale generation

**Why Multiple Base Colors**: Each color family needs its own starting point to generate distinct but systematically related color scales.

### 2. Generating parallel color scales

Once we have both base colors, we need to generate separate color scales for each. This requires using multiple Scale Colors nodes working in parallel.

**Blue Scale Generation:**

<figure><img src="../.gitbook/assets/Screenshot 2025-06-12 at 6.12.54 PM (1).png" alt=""><figcaption></figcaption></figure>

* Drag a **Scale Colors** node into your graph
* Connect the output from your **blue Constant** node to the `color` input
* Configure the scale parameters:
  * Set `stepsUp` to `5` (5 lighter shades above base)
  * Set `stepsDown` to `5` (5 darker shades below base)
* The output will be an array of 11 blue colors from lightest to darkest

**Red Scale Generation:**

<figure><img src="../.gitbook/assets/Screenshot 2025-06-12 at 6.12.09 PM.png" alt=""><figcaption></figcaption></figure>

* Drag a second **Scale Colors** node into your graph
* Connect the output from your **red Constant** node to the `color` input
* Configure with identical parameters:
  * Set `stepsUp` to `5` (5 lighter shades above base)
  * Set `stepsDown` to `5` (5 darker shades below base)
* The output will be an array of 11 red colors from lightest to darkest

**Parallel Processing**: Both color scales are generated simultaneously, maintaining consistency in the number of steps while producing distinct color families.

### 3. Token Creation (Multiple Array Map Subgraphs)

We now have two separate arrays of colors that need to be converted into design tokens. Each color family requires its own Array Map with a subgraph configured for that specific color name.



**Blue Token Creation:**

* Drag an **Array Map** node and connect the blue Scale Colors output to its `array` input
* Double-click the Array Map to enter the **Subgraph Explorer**

**\[IMAGE: Screenshot showing the blue Array Map subgraph with all internal nodes]**

Configure the blue subgraph with these nodes:

* **Input** node (provides `value`, `index`, `length`)
* **Color to string** node (connect `value` from Input)
* **Numeric Scale** node (connect `index` from Input, set `multiplier` to `100`, `prefix` to `"blue."`)
* **Create Design Token** node (connect name from Numeric Scale, value from Color to string, set type to `"color"`)
* **Output** node (connect from Create Design Token, set type to `"any"`)

**Red Token Creation:**

* Drag a second **Array Map** node and connect the red Scale Colors output to its `array` input
* Configure an identical subgraph but change the **Numeric Scale** `prefix` to `"red."`

**\[IMAGE: Screenshot showing the red Array Map subgraph with "red." prefix configuration]**

**Result**: Each Array Map produces tokens like `blue.100`, `blue.200`... and `red.100`, `red.200`... respectively.

### 4. Combining multiple token arrays

After creating tokens for each color family, we need to combine them into a single unified array for final processing.

**\[IMAGE: Screenshot showing Arrify and Array flatten nodes combining the two token arrays]**

**Merging Arrays:**

* Drag an **Arrify** node into your graph
* Connect the output from the **blue Array Map** to one input
* Connect the output from the **red Array Map** to another input
* Drag an **Array flatten** node and connect the Arrify output to it

**What This Does**: The Arrify node combines both token arrays into a nested structure, then Array flatten merges them into one continuous array containing all blue and red tokens.

### 5. Final token set formatting

**\[IMAGE: Screenshot showing Array of Tokens to Set node connected to the flattened array]**

**Converting to Token Set:**

* Drag an **Array of Tokens to Set** node
* Connect the flattened array output to the `tokens` input
* This converts the array format into a proper token set structure

### 6. Final Output

**\[IMAGE: Screenshot showing the Output node and the final table result]**

**Output Configuration:**

* Drag an **Output** node and connect the token set to it
* The final result will be a comprehensive token set containing both color families

**Final Result:**\
The completed workflow generates a systematic token set with:

* `blue.100` through `blue.1100` (11 blue tokens)
* `red.100` through `red.1100` (11 red tokens)
* **Total: 22 design tokens** in one unified workflow

**\[IMAGE: Screenshot showing the complete final graph with all connections]**

```json
{
  "blue.100": "#e5e7eb",
  "blue.200": "#c5cdde", 
  "blue.300": "#9fb8d3",
  "blue.400": "#7391c8",
  "blue.500": "#4169bd",
  "blue.600": "#1d4ed8",
  "blue.700": "#1e40af",
  "blue.800": "#1e3a8a",
  "blue.900": "#1e3a8a",
  "blue.1000": "#312e81",
  "blue.1100": "#1e1b4b",
  "red.100": "#fee2e2",
  "red.200": "#fecaca",
  "red.300": "#fca5a5",
  "red.400": "#f87171",
  "red.500": "#ef4444",
  "red.600": "#dc2626",
  "red.700": "#b91c1c",
  "red.800": "#991b1b",
  "red.900": "#7f1d1d",
  "red.1000": "#651e1e",
  "red.1100": "#4a1e1e"
}
```

**Scalability**: This workflow can easily be extended by adding more Constant→Scale Colors→Array Map chains for additional color families like green, purple, yellow, etc.
