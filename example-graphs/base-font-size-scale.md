---
hidden: true
---

# Base Font Size Scale

Creates a systematic font size token system using harmonic progression. This multi-step workflow generates mathematically-related font sizes that maintain visual harmony, then converts them into properly named design tokens with hierarchical organization.

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.00.21 PM.png" alt=""><figcaption><p>Base Font Scale</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.07.04 PM (1).png" alt=""><figcaption><p>Table Output</p></figcaption></figure>

#### Step 1: Base Value Setup

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.34.44 PM.png" alt=""><figcaption></figcaption></figure>

1. Drag a Constant node into your graph.
2. Important: Click the type dropdown and select "Number" from the available options.
3. Set the value input to 16 (your base font size in pixels).
4. The node will output the number value ready for mathematical operations.

Configuration:

* Input: value → 16 (Number type)
* Output: value → 16

#### Step 2: Harmonic Series Generation

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.37.42 PM.png" alt=""><figcaption></figcaption></figure>



1. Drag a Harmonic Series node into your graph.
2. Connect the output from your Constant node to the base input.
3. Configure the remaining inputs as shown below to create a balanced font scale.

Input Configuration:

* base → 16 (connected from Constant node) - Your foundation font size
* stepsDown → 0 - No smaller sizes below the base (keeps 16px as the smallest)
* stepsUp → 5 - Generate 5 additional larger sizes above the base
* notes → 5 - Use 5 intervals within each octave for finer gradation
* ratio → 2 - Use a 2:1 ratio (musical octave) for harmonic progression
* precision → 0 - Round to whole numbers (no decimals for pixel values)

Expected Output:

* array → \[16, 18, 21, 24, 28, 32] (6 items total)

#### Step 3: Token Creation Setup (Array Map)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-05 at 8.40.43 PM.png" alt=""><figcaption></figcaption></figure>

1. Drag an Array Map node into your graph.
2. Connect the array output from your Harmonic Series node to the array input of the Array Map.
3. Important: You'll need to double-click the Array Map node or click "Subgraph Explorer" to configure the internal logic.

Input Configuration:

* array → \[16, 18, 21, 24, 28, 32] (connected from Harmonic Series)



#### Step 3a: Array Map Input Node (Inside Subgraph)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 2.58.31 PM.png" alt=""><figcaption><p>Inside the subgraph explorer</p></figcaption></figure>

Input (inside Array Map subgraph)\
What This Node Provides:This is the starting point of your Array Map subgraph. The Array Map automatically provides three special values for each font size it processes:Available Outputs:

* value → 16 (the current font size being processed from the next connected stringify node)
* index → 5 (the position in the array, starting from 0)
* length → 6 (total number of items in the array)

**Step 3b: Convert Font Size to String (Stringify)**

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.38.07 PM.png" alt=""><figcaption><p>Stringify </p></figcaption></figure>

Node: Stringify (inside Array Map subgraph)

1. Drag a Stringify node into your subgraph.
2. Connect the value output from the Input node to the value input of the Stringify node.

Input Configuration:

* value → 32 (connected from Input node - the current font size being processed)

What This Node Does:Converts the numeric font size into a string format. Design tokens typically store values as strings, so this conversion ensures compatibility with the token system.Conversion Example:

* Input: 32 (number)
* Output: "32" (string)

#### Step 3c: Generate Systematic Token Names (Numeric Scale)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.40.29 PM.png" alt=""><figcaption><p>Numeric Scale</p></figcaption></figure>

Node: Numeric Scale (inside Array Map subgraph)

1. Drag a Numeric Scale node into your subgraph.
2. Connect the index output from the Input node to the index input of the Numeric Scale.
3. Configure the remaining inputs to create your naming pattern.

Input Configuration:

* index → 5 (connected from Input node - the current position in the array)
* multiplier → 1 (no scaling needed, just use sequential numbers)
* prefix → "size-" (text to add before the number)
* suffix → (empty - no text needed after the number)

#### Step 3d: Assemble the Complete Design Token (Create Design Token)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.45.47 PM.png" alt=""><figcaption></figcaption></figure>

Node: Create Design Token (inside Array Map subgraph)

1. Drag a Create Design Token node into your subgraph.
2. Connect the outputs from previous nodes to assemble the complete token.
3. Set the token type using the dropdown.

Input Configuration:

* name → "size-6" (connected from Numeric Scale output)
* type → "dimension" (select from dropdown - appropriate for font sizes)
* value → "32" (connected from Stringify output)
* description → (leave empty or add optional description)
* $extensions → null (leave as default for basic tokens)

Expected Output:

* token → Complete token: size-6 → 32 (ready for use in design systems)

#### Step 3e: (Output)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 3.47.26 PM.png" alt=""><figcaption><p>Output</p></figcaption></figure>

Node: Output (inside Array Map subgraph):

1. The Output node should already be present in your subgraph.
2. Important: Set the output type to "Any" to handle token objects properly.
3. Connect the token output from Create Design Token to this Output node.

Configuration:

* Type: Any (allows token objects to pass through)
* Input: Connect token object from Create Design Token

#### Step 4: Add Hierarchical Namespace (Group Token Array)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 4.40.07 PM.png" alt=""><figcaption></figcaption></figure>

Node: Group Token ArrayHow to Configure:

1. Drag a Group Token Array node into your graph.
2. Connect the value output from Array Map to the tokens input.
3. Set the namespace for organizing your tokens.

Input Configuration:

* name → "fontSize" (the namespace to add to all token names)
* tokens → Array of tokens from Array Map (size-1, size-2, etc.)

What This Node Does:Adds a namespace prefix to all token names, creating a hierarchical organization. Each token name gets prefixed with "fontSize." to group them logically.Name Transformation:

* "size-1" → "fontSize.size-1"
* "size-2" → "fontSize.size-2"
* "size-3" → "fontSize.size-3"
* "size-4" → "fontSize.size-4"
* "size-5" → "fontSize.size-5"
* "size-6" → "fontSize.size-6"

#### Step 5: Convert to Token Set Format (Array of Tokens to Set)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 4.41.40 PM.png" alt=""><figcaption></figcaption></figure>

Node: Array of Tokens to SetHow to Configure:

1. Drag an Array of Tokens to Set node into your graph.
2. Connect the tokens output from Group Token Array to the tokens input.

Input Configuration:

* tokens → Namespaced token array from Group Token Array

Expected Output:

* tokenSet → Structured token set ready for export and use

#### Step 6: Final System Output (Output)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 4.42.52 PM.png" alt=""><figcaption></figcaption></figure>

Node: OutputHow to Configure:

1. The Output node should already be present in your graph.
2. Connect the tokenSet output from Array of Tokens to Set to the Output node.

Input Configuration:

* tokenSet → Complete hierarchical token set from previous step

\




\


\










