# Add (Variadic)

The **Add (Variadic) node** is a **Math node** that allows you to sum multiple numbers dynamically. You can find it under the **Math Nodes** category. You can also search for the node using the top search bar in the **Nodes panel** or use the keyboard shortcut **Shift + K**.

### Using the Add (Variadic) Node

Unlike the standard **Add node**, which only accepts two inputs, the **Add (Variadic) node** supports multiple inputs, making it useful for summing multiple values in a single operation.

1. **Drag the Add (Variadic) node** into the canvas.
2. **Check the input panel** – it allows you to add multiple number inputs dynamically.
3. **Check the output panel** – it outputs a **single number**, which is the sum of all input values.
4. **Enable inline types and values** to visualize the values passing through the node.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 18.38.37@2x.png" alt=""><figcaption></figcaption></figure>

### Example Usage

1. Drag an **Add (Variadic) node** onto the canvas.
2. Drag four **Constant nodes** onto the canvas.
3. In each **Constant node’s** input panel, set the type to **Number** and enter values, e.g., 3, **5, 7, and 9**.
4. Connect the **outputs** of all four Constant nodes to the inputs of the **Add (Variadic) node**.
5. The **output panel** of the Add (Variadic) node should display **24** (3 + 5 + 7 + 9).

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 18.42.50@2x.png" alt=""><figcaption></figcaption></figure>

### Adding More Inputs

* By default, the node has a number array as the input port.
* Connecting an edge to the input port adds additional input slots as needed.
* The sum updates automatically as more inputs are added.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 18.50.57.gif" alt=""><figcaption></figcaption></figure>

