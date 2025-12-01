# Closest Number

The **Closest Number node** is a **Math node** that finds the closest value in an array of numbers to a given target number. You can find it under the **Math Nodes** category. You can also search for the node using the top search bar in the **Nodes panel** or use the keyboard shortcut **Shift + K**.

### Inputs

* **Array of Numbers** – A list of numbers to compare against.
* **Target Number** – The number for which the closest match is to be found.

### Outputs

* **Index** – The position of the closest number in the array.
* **Value** – The closest number from the array.
* **Difference** – The difference between the target number and the closest value.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 19.23.59@2x.png" alt=""><figcaption></figcaption></figure>

### Using the Closest Number Node

1. **Drag the Closest Number node** onto the canvas.
2. **Check the input panel** – it requires an **array of numbers** and a **target number**.
3. **Check the output panel** – it provides the **index**, **closest value**, and **difference**.
4. **Enable inline types and values** to see the data passing through the node.

### Example Usage

1. Drag a **Closest Number node** onto the canvas.
2. Drag an **Arithmetic Series node** onto the canvas to generate an array of numbers.
3. Set the **base value**, **step down, step up, increment  and precision** in the Arithmetic Series node (e.g., start at **5**, step down 0, step up 5, increment by 5, precision 0 will generate **10 numbers** → output: `[5, 10, 15, 20, 25, 30, 35]`).
4. Connect the **output** of the Arithmetic Series node to the **Array of Numbers** input of the Closest Number node.
5. Drag a **Constant node**, set its type to **Number**, and enter a target number, e.g., **17**.
6. Connect the **output** of the Constant node to the **Target Number** input of the Closest Number node.
7. The **output panel** of the Closest Number node should display:
   * **Index:** `2` (since `15` is at index 2 in the array)
   * **Value:** `15` (the closest number to 17)
   * **Difference:** `2` (difference between 17 and 15)

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-18 at 19.40.39@2x.png" alt=""><figcaption></figcaption></figure>

