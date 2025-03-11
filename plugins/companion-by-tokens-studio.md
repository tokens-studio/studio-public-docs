# Companion by Tokens Studio

**Companion by Tokens Studio** is a Figma plugin designed to seamlessly sync and consume design tokens from Tokens Studio as variables in Figma. It ensures your design tokens are always structured and accessible within your Figma files, reflecting updates made in Studio.

<figure><img src="../.gitbook/assets/Companion Plugin.png" alt=""><figcaption></figcaption></figure>

### Setting Up Companion by Tokens Studio

{% stepper %}
{% step %}
#### Install and Launch the Plugin

* Open your Figma design file.
* Navigate to **Plugins > Companion by Tokens Studio** and run the plugin.
{% endstep %}

{% step %}
#### Syncing Tokens from Tokens Studio

To set up the connection and sync your tokens:

1. **Configure the API Key**:
   * Refer to the Tokens Studio [API Keys](https://tokens.studio/platform) section to generate an API key.
   * Paste the API key into the Companion plugin interface.
   * Select your organization and project to complete the connection.
2. **View Tokens**:
   * Once synced, all design tokens created in Tokens Studio will be visible in the Companion plugin.
   * Tokens are organized by **collections** and **modes** (modes) which corresponds to Theme Groups and Theme Options in Studio.

<figure><img src="../.gitbook/assets/Api key to companion.gif" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Creating Variables in Figma

1. In your Figma file, navigate to the bottom of the Companion plugin interface and click **Create**.
2. Variables will be generated in Figma, replicating the structure of your tokens in Studio:
   * Theme Groups as Collections.
   * Theme options structured as modes.

<figure><img src="../.gitbook/assets/Export Tokens to Figma Variables Companion Plugin.gif" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

### Updating and Monitoring Tokens

#### Fetching Updates from Studio

* If changes are made in Studio, click **Fetch from Studio** in the plugin to sync the updates.
* Click **Create** again to generate the updated variables in Figma. Only the differential updates will be applied.

<figure><img src="../.gitbook/assets/Fetch Updates.png" alt=""><figcaption></figcaption></figure>

#### Watch Mode

* Activate **Watch Mode** by clicking the **Watch Icon** in the plugin.
  * This minimizes the plugin but monitors changes in Studio.
  * Every 5 seconds, updates in Studio are automatically fetched and applied in Figma.
* To stop Watch Mode, simply deactivate it by clicking the cancel button.

<figure><img src="../.gitbook/assets/Watch Mode Companion.gif" alt=""><figcaption></figcaption></figure>

### Managing Variables

* **Delete Variables**: Use the **Delete Variables** button to remove all variables created through the plugin in the current Figma file.

