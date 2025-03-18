# Absolute Node

The **Absolute node** is a **Math node**. You can find it under the **Math Nodes** category. You can also search for the node using the top search bar in the **Nodes panel** or use the keyboard shortcut **Shift + K**.

#### Using the Absolute Node

The **Absolute node** takes a single number as input and returns its **absolute value**, which means it removes any negative sign and outputs a non-negative number.

1. **Drag the Absolute node** into the canvas.
2. **Check the input panel** – the node takes **one number** as input.
3. **Check the output panel** – it outputs a **non-negative number**, which is the absolute value of the input.
4. **Enable inline types and values** to see the data flowing through the node.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-18 at 18.32.43@2x.png" alt=""><figcaption></figcaption></figure>

#### Example Usage

1. Drag an **Absolute node** onto the canvas.
2. Drag a **Constant node** onto the canvas.
3. In the **Constant node's** input panel, set the type to **Number** and enter a negative value, e.g., **-100**.
4. Connect the **output** of the Constant node to the input of the Absolute node.
5. Check the **output panel** of the Absolute node – it should display 100 (the absolute value of -100).
6. Drag a **Preview > Number node** and connect the input to the output of the **Absolute node**, it will display 100.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-18 at 18.32.03@2x.png" alt=""><figcaption></figcaption></figure>
