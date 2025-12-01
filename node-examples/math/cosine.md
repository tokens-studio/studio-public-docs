# Cosine

The **Cosine node** is a **Math node** that calculates the cosine of an input angle. You can find it under the **Math Nodes** category. You can also search for the node using the top search bar in the **Nodes panel** or use the keyboard shortcut **Shift + K**.

### Inputs

* **Angle (Number)** – The angle in **radians** for which to compute the cosine.

### Output

* **Cosine Value (Number)** – The result of the cosine function, ranging from `-1` to `1`.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 19.42.46@2x.png" alt=""><figcaption></figcaption></figure>

### Using the Cosine Node

1. **Drag the Cosine node** onto the canvas.
2. **Check the input panel** – it requires an **angle** in radians.
3. **Check the output panel** – it returns the **cosine of the input angle**.
4. **Enable inline types and values** to visualize the data passing through the node.

### Example Usage

1. Drag a **Cosine node** onto the canvas.
2. Drag a **Constant node** onto the canvas.
3. In the **Constant node’s** input panel, set the type to **Number** and enter a value in radians, e.g., **3.14** (π radians).
4. Connect the **output** of the Constant node to the **Angle** input of the Cosine node.
5. The **output panel** of the Cosine node should display **-1**, since `cos(π) = -1`.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 20.10.56@2x.png" alt=""><figcaption></figcaption></figure>

### Converting Degrees to Radians

If you have an angle in degrees, use a **Multiply node** to convert it to radians:

* Multiply the degree value by `π / 180` to convert it to radians before feeding it into the **Cosine node**.
