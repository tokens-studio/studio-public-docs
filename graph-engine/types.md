# Types

Every node port in the Graph Engine, whether it's an input or output, is **strongly typed**. This means that each port is designed to work with only one specific kind of data.

### What does "Strongly Typed" mean?

Think of a port like a specialized container - a `number` input can only accept numerical values (like 12, 42.5, 0.432, etc.), while a `color` port is specifically designed for color values (hex, rgba, hsl, p3, etc.). Trying to connect incompatible types, such as sending a color to a number input, won't work.

#### Benefits of Strong Typing

This approach keeps your graphs reliable by:

* **Preventing common mistakes** - The Graph Engine stops you from making connections that don't make sense (like trying to perform math operations on text)
* **Ensuring consistent outputs** - Your design tokens and generated code remain predictable
* **Simplifying troubleshooting** - When something goes wrong, it's easier to find where the problem is

## Supported Types You'll Encounter

<table><thead><tr><th width="136.296875">Name</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td>Number</td><td>Integers or decimals</td><td>5, 3.14, 0.025</td></tr><tr><td>String</td><td>Text strings, special characters or text with spaces.</td><td>"bold", "#FF5733"</td></tr><tr><td>Color</td><td>Color objects such as RGB, HSL etc. formats.</td><td>rgb(76, 190, 66), hsl(67, 96, 65)</td></tr><tr><td>Array</td><td>Lists of values (contains multiple items of the same type)</td><td>[10, 20, 30], ["#263724", "#ED8DF0"]</td></tr><tr><td>Object</td><td>Collections of related values with names in the format of "key" : "value".</td><td>{ "foreground": "#177BF7"}</td></tr><tr><td>Boolean</td><td>True or False. Useful for decisions to your logic with the <a data-mention href="available-nodes/logic/">logic</a> node.</td><td>true, false</td></tr><tr><td>Curve</td><td>A </td><td></td></tr><tr><td>Token</td><td>A design token that meets the DTCG format.</td><td></td></tr><tr><td>Token Set</td><td>A special type for design token collections</td><td></td></tr><tr><td>Any</td><td>An agnostic type value that you probably don't want to use.</td><td></td></tr></tbody></table>

## How to Identify Port Types in the Graph Engine

Ports use both colors and shapes to indicate what type of data they accept or output:

### Color Coding

Each type has a distinct color associated with it:

| Color    | Data Type |
| -------- | --------- |
| Blue     | Number    |
| Green    | String    |
| Red      | Color     |
| Orange   | Boolean   |
|  Magenta | Curve     |
| Teal     | Object    |
| Yellow   | Array     |
| Purple   | Any       |

### **Shape Indicators**

Ports also use shapes to indicate whether they handle single values or collections:

* **Circle/Dot** (●): Accepts or outputs a single value (e.g., one color, one number)
* **Square** (■): Accepts or outputs an array/list of values (e.g., a list of colors)

{% hint style="info" %}
Hovering over a port shows its type label (e.g., "color") if "Port Types" is enabled in settings.
{% endhint %}

## Displaying Labels for Port Types

You can display the labels for all ports to easily identify the type. This can be done from clicking the "Settings" icon on the Top Bar and enabling Show Inline Types.

<figure><img src="../.gitbook/assets/2025-05-08 at 12.52.19 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>

## Converting Types

Mismatched types block connections, but conversion nodes fix this:

* **Why It’s Needed**:
  * Example: A "Color Generator" outputs a color object, but a "Create Design Token" needs a hex string. They won’t connect directly.
* **How to Convert**:
  * **Scenario**: Convert a color to a hex string.
    1. Connect the "Create Color" output (color) to a "Color to String" node’s input.
    2. The node outputs a hex string (e.g., "#FF5733").
    3. Plug this into the "Create Design Token" input, which now works.
  * **Other Conversions**: "Stringify" (e.g., 10 → "10").

<figure><img src="../.gitbook/assets/Type Conversion.png" alt=""><figcaption></figcaption></figure>
