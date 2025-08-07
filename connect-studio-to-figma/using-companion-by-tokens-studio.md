# Using Companion by Tokens Studio

Companion by Tokens Studio is a Figma plugin which is meant purely for consumption of design tokens from Studio as variables in Figma.

**Prerequisites**:

* [api-keys.md](../settings/api-keys.md "mention")



{% stepper %}
{% step %}
### Open a Figma design file

This can be a new empty file to ensure that your production design files are not affected while setting up a connection between Studio and Figma.
{% endstep %}

{% step %}
### Install/Launch the plugin

1. Go to plugins > Companion by Tokens Studio.
2. Run the plugin.
{% endstep %}

{% step %}
### Setting up Studio sync

1. Return to Studio.
2. Click on Find your API key. You can also jump to the API keys page by using the keyboard shortcut cmd+k.
3. The API key is linked to the user which means that it gives access to all the Organisations and Projects that a user is part of.&#x20;

For more info read [Platform > API keys](../settings/api-keys.md).

<figure><img src="../.gitbook/assets/Find API Key.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### &#x20;Creating your API key

1. Click on create a new key.
2. Give your API key a name.
3. (Optional) Give your API key a description.
4. Click create.
5. Copy your API key.&#x20;

IMPORTANT: Your API key will not be visible again, so make sure to copy it.

<figure><img src="../.gitbook/assets/Create API Key.gif" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Syncing to Companion by Tokens Studio

1. Return to Figma and the plugin.
2. Enter your API key.
3. Choose the Organisation that you want to connect.
4. Choose the Project that you want to connect.
5. You are now connected to Studio and your tokens should reflect in the plugin.

<figure><img src="../.gitbook/assets/Api key to companion.gif" alt=""><figcaption></figcaption></figure>

For more information on the features of Companion by Tokens Studio, see [Companion by Tokens Studio](../plugins/companion-by-tokens-studio.md).
{% endstep %}
{% endstepper %}
