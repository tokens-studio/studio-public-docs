# Using Tokens Studio for Figma

**Prerequisites**:

* [api-keys.md](../settings/api-keys.md "mention")

{% stepper %}
{% step %}
### Open a Figma design file

This can be an empty file to ensure that your production designs are not affected while setting up connection with Studio.
{% endstep %}

{% step %}
### Install/Launch Tokens Studio for Figma

1. Go to Plugins > Tokens Studio for Figma.
2. In the plugin’s interface, open a "New empty file".

<div><figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 3.37.32 PM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 3.53.08 PM.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
### Adding a new sync provider

1. Open the Settings tab on the plugin.
2. Click on Add new sync provider.
3. Select Token Studio from the list.

<div><figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.26.29 PM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.30.12 PM (1).png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
### Setting up Token Studio sync

1. Return to Studio and go to the dashboad on the left panel.
2. Click on Find your API key. You can also jump to the API keys page by using the keyboard shortcut cmd+k.
3. The API key is linked to the user which means that it gives access to all the Organisations and Projects that a user is part of.&#x20;

For more info read [Platform > API keys](../settings/api-keys.md).

<figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.33.04 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Creating your API key

1. Click on create an api key.
2. Give your API key a name.
3. Select the necessary scopes ( [api-keys.md](../settings/api-keys.md "mention")for more details on what scope to choose)
4. Click create token.
5. Copy your API key.&#x20;

IMPORTANT: Your API key will not be visible again, so make sure to copy it.

<div><figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.39.58 PM (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.41.06 PM.png" alt=""><figcaption></figcaption></figure></div>

<figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.41.29 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Finish adding Studio sync on the plugin

1. Return to Figma, on the plugin click on the sync provider we just created
2. Give a name for the sync for easy identification.
3. Enter the API key we just copied in the Personal Access Token field.
4. Choose the Organisation that you want to connect.
5. Choose the Project that you want to connect.
6. You are now connected to Studio and your tokens should reflect in the plugin under the Tokens tab

<div><figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.55.08 PM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Screenshot 2025-11-21 at 4.53.10 PM.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
### Bi-directional syncing

1. Connection with Studio and the plugin is a bi-directional sync.
2. Any changes on Studio can be pulled in the plugin by clicking on sync icon at the bottom left of the plugin.
3. Any changes on the plugin will be automatically updated on the studio.&#x20;
{% endstep %}
{% endstepper %}
