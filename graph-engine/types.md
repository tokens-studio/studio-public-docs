# Types

### Why Strong Typing Matters

Every port in the Graph Engine is **strongly typed**, meaning it only accepts specific data types (e.g., a "number" port won’t take a "color"). This keeps your graphs reliable by:

* Catching mistakes early (e.g., no connecting a string to a math node).
* Ensuring predictable outputs for design tokens or code.
* Making complex systems easier to debug and scale.

### What Are Types?

Types define what kind of data a port handles—like "number" for 42, "color" for #FF5733, or "array" for a list. They’re the rules that keep your graph running smoothly.

#### How to Identify the Type of an Input or Output

Ports use visual cues:

* **Colors**: Show the type (see legend from the Top Action Bar > Layout > Legend ):
  * Red: Color
  * Magenta: Curve
  * Green: String
  * Gold: Boolean
  * Blue: Number
  * Teal: Object
  * Purple: Any
* **Shapes**:
  * **Dot**: Single value (e.g., one color).
  * **Square**: Array (e.g., list of colors). Hovering over a port shows its type label (e.g., "color") if "Port Types" is enabled in settings.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

### Supported Types

Here’s what you’ll work with:

* **Number**: Integers or decimals (e.g., 5, 3.14).
* **String**: Text (e.g., "bold", "#FF5733").
* **Color**: Color objects (e.g., RGB, HSL formats).
* **Array**: Lists (e.g., \[10, 20, 30], \["#FF5733", "#33FF57"]).
* **Object**: Key-value pairs (e.g., { "primary": "#FF5733" }).
* **Boolean**: True/false.
* **Token Set**: A special type for design token collections (e.g., a JSON-like structure).

### Type Conversion

Mismatched types block connections, but conversion nodes fix this:

* **Why It’s Needed**:
  * Example: A "Color Generator" outputs a color object, but a "Create Design Token" needs a hex string. They won’t connect directly.
* **How to Convert**:
  * **Scenario**: Convert a color to a hex string.
    1. Connect the "Color Generator" output (color) to a "Color to String" node’s input.
    2. The node outputs a hex string (e.g., "#FF5733").
    3. Plug this into the "Create Design Token" input, which now works.
  * **Other Conversions**: "Stringify" (e.g., 10 → "10").

<figure><img src="../.gitbook/assets/Type Conversion.png" alt=""><figcaption></figcaption></figure>
