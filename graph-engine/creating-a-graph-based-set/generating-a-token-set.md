---
description: How to export a design token set through the Graph Editor.
---

# Generating a Token Set

Similar to static token sets, a graph-based set needs to define what tokens to be included, and what their values are.

To define the tokens of the token set, we need to generate a token set and set it as the output of the graph.&#x20;

## What is a token set?

A token set is an object that contains the definitions of a single, or multiple design tokens. For example, a set of tokens that contain hex values, or font-size values.

## Basic Example

{% stepper %}
{% step %}
### Create a design token

To create a design token that will be included in a token set, use the [create-design-token.md](../available-nodes/design-tokens/create-design-token.md "mention") node. Here, you can give your token a name, set the type and apply a value to it. You can set the values of each input manually, or use other nodes such as [interpolation.md](../available-nodes/string/interpolation.md "mention") or [constant.md](../available-nodes/generic/constant.md "mention").

{% hint style="info" %}
There are of course many ways to generate the value of a token, and creating a design token may happen elsewhere in the flow, but the intention is the same.
{% endhint %}

<figure><img src="../../.gitbook/assets/2025-05-08 at 10.57.19 - Screengrab@2x.png" alt=""><figcaption><p>Defining a design token using the Create Design Token node.</p></figcaption></figure>
{% endstep %}

{% step %}
### Create an array of design tokens

To turn a token, or many, into a token set, first we need to build an array with them. Using the [arrify.md](../available-nodes/array/arrify.md "mention") node, you can build an array by defining your design tokens as the input.

<figure><img src="../../.gitbook/assets/2025-05-08 at 11.06.18 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Convert Array to Token Set

Now that you have an array of tokens, we need to turn it into a Token Set that we can output. Use the [array-to-set.md](../available-nodes/design-tokens/array-to-set.md "mention") node to turn the output of the Arrify node (currently an array of tokens), into a Token Set. You'll see that the output of the node is an object in the token format.

<figure><img src="../../.gitbook/assets/2025-05-08 at 11.09.40 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Output your Token Set

To capture the output of the graph and generate a tokenset, add an input named "tokenSet" and set the type to `any` . This will allow you to generate a token set, and export it directly.&#x20;

<figure><img src="../../.gitbook/assets/2025-05-08 at 10.33.28 - Screengrab@2x.png" alt=""><figcaption><p>An output node with an input set to "tokenSet" and the type set to "any".</p></figcaption></figure>

Next, connect the output of the [array-to-set.md](../available-nodes/design-tokens/array-to-set.md "mention") node to your new tokenSet input

<figure><img src="../../.gitbook/assets/2025-05-08 at 11.12.44 - Screengrab@2x.png" alt=""><figcaption><p>Our entire graph where we create design tokens, group them in an array, turn the array into a set and then output them.</p></figcaption></figure>

You'll now see your tokens presented with their resolved values in the table view of the set.

<figure><img src="../../.gitbook/assets/2025-05-08 at 11.14.30 - Screengrab@2x.png" alt=""><figcaption><p>Our outputted tokens in the table view of a Graph-Based set.</p></figcaption></figure>
{% endstep %}
{% endstepper %}
