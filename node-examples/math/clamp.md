# Clamp

The **Clamp node** is a **Math node** that restricts a number within a specified range. You can find it under the **Math Nodes** category. You can also search for the node using the top search bar in the **Nodes panel** or use the keyboard shortcut **Shift + K**.

### Using the Clamp Node

The **Clamp node** takes three inputs:

* **Value** – the number to be clamped.
* **Min** – the lower bound of the range.
* **Max** – the upper bound of the range.

It outputs the input value if it falls within the range. If the value is lower than **Min**, it returns **Min**. If the value is higher than **Max**, it returns **Max**.

1. **Drag the Clamp node** into the canvas.
2. **Check the input panel** – it requires a **value**, a **min** limit, and a **max** limit.
3. **Check the output panel** – it returns the clamped value.
4. **Enable inline types and values** to visualize the data flow.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 19.04.12@2x.png" alt=""><figcaption></figcaption></figure>

### Example Usage

1. Drag a **Clamp node** onto the canvas.
2. Drag three **Constant nodes** onto the canvas.
3. In the first **Constant node**, set the type to **Number** and enter a test value, e.g., **12**.
4. In the second **Constant node**, set the type to **Number** and enter the **Min** value, e.g., **5**.
5. In the third **Constant node**, set the type to **Number** and enter the **Max** value, e.g., **10**.
6. Connect the outputs of the three Constant nodes to the corresponding inputs of the **Clamp node**.
7. The **output panel** of the Clamp node should display **10**, since 12 exceeds the maximum limit of 10.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 19.19.27@2x.png" alt=""><figcaption></figcaption></figure>

8. In the first **Constant node** change the value from **12** to **8**.
9. The output panel of the **Clamp node** should display **8**, since **8** falls in between the limits.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 19.19.58@2x.png" alt=""><figcaption></figcaption></figure>

### When to Use

The **Clamp node** is useful when working with dynamic values where you need to ensure they stay within a valid range.
