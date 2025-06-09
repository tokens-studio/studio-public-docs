# Color scale

#### What It Does

Creates a systematic color palette using algorithmic color scaling. This multi-step workflow generates a complete color scale from a single base color, then converts each shade into properly named design tokens with hierarchical organization.

#### Complete Workflow

This example demonstrates a 6-step process that transforms a single base color into a complete token system:

1. Base Color Setup: Define the starting color
2. Color Scale Generation: Create algorithmically related shades
3. Token Creation: Convert each color into a named token
4. Namespace Grouping: Add hierarchical prefixes
5. Set Conversion: Format for token system output
6. Final Export: Output structured token set

#### Step 1: Base Color Setup

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 8.43.36 PM.png" alt=""><figcaption></figcaption></figure>

Node: ConstantHow to Configure:

1. Drag a Constant node into your graph.
2. Important: Click the type dropdown and select "Color" from the available options.
3. Set your base color value (the color that all other shades will be generated from).
4. The node will output the color value ready for scale generation.

Configuration:

* Input: value → Base color (Color type)
* Output: value → Base color for scale generation

Why Color Type Matters: Setting the type to "Color" ensures the Scale Colors node can perform proper color calculations and transformations.

#### Step 2: Color Scale Generation

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 8.44.27 PM.png" alt=""><figcaption></figcaption></figure>

Node: Scale Colors

How to Configure:

1. Drag a Scale Colors node into your graph.
2. Connect the output from your Constant node to the color input.
3. Configure the scale parameters to create your desired range.

Expected Input Configuration:

* color → Base color (connected from Constant node)
* stepsUp → Number of lighter shades to generate
* stepsDown → Number of darker shades to generate

Expected Output: array → Complete color scale from lightest to darkest (11 colors total)What This Creates: An algorithmic color scale that maintains visual consistency while providing a full range from very light tints to very dark shades of your base color.

#### Step 3: Token Creation (Array Map Subgraph)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 8.37.23 PM.png" alt=""><figcaption></figcaption></figure>

3a. Input Node( inside the subgraph)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 9.10.14 PM.png" alt=""><figcaption></figcaption></figure>

* Receives: value (color), index (position), length (total count)
* Example: value = #181212, index = 10, length = 11

3b. Name Generation (Numeric Scale):

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 9.11.03 PM.png" alt=""><figcaption></figcaption></figure>

* index → 10
* multiplier → 100 (creates 100-scale naming)
* prefix → "red." (color name prefix)
* suffix → "" (empty)

Output: value → "red.1100" (calculation: (10+1)100 = 1100)

3c. Color Conversion (Color to String)Input: Color value → #181212Configuration: space → "hex" (hexadecimal format)Output: value → "#181212" (hex string format)

3d. Token Assembly (Create Design Token)

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 9.12.23 PM.png" alt=""><figcaption></figcaption></figure>

Inputs:

* name → "red.100" (from Numeric Scale)
* type → "color"
* value → "#181212" (from Color to String)



Array Map Final Output: Array of color tokens with systematic naming

#### Step 4: Namespace Grouping

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 8.45.42 PM.png" alt=""><figcaption></figcaption></figure>

Node: Group Token Array

* name → "color"
* tokens → Token array from Array Map

Name Transformation:

* "red.100" → "color.red.100"
* "red.200" → "color.red.200"
* ...continuing through the full scale

#### Step 5: Array of tokens to set

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 9.32.22 PM.png" alt=""><figcaption></figcaption></figure>

\
Step 6: Output Node

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 9.33.48 PM.png" alt=""><figcaption></figcaption></figure>



#### Final Result

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 9.35.58 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-06-06 at 5.06.59 PM.png" alt=""><figcaption></figcaption></figure>

