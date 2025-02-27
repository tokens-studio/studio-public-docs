# Import from Figma variables

If you already have design tokens or variables in Figma, you can easily import them into Studio. Below is an example workflow using the Tokens Studio for Figma plugin.

### Export from Figma



{% stepper %}
{% step %}
### Open Figma and Your Design File

In Figma, ensure you have set up Figma Variables that you want to migrate.
{% endstep %}

{% step %}
### Install/Launch the Tokens Studio for Figma Plugin

1. Go to Plugins > Tokens Studio for Figma.
2. In the plugin’s interface, open a "New empty file".

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Import Figma Variables

1. In the plugin, look for an Import Variables button.
2. Choose whether to convert numbers to dimensions, use rem values, etc.
3. Click Import.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

_Tip: You might see collections such as “foundation” or “light” and “dark” in Figma, which will become token sets groups and the modes will become token sets in Studio. The Figma collections will be mapped as Theme Groups and modes as Theme Options in Studio._
{% endstep %}

{% step %}
### Export to a Zip File

1. In the bottom-left of the plugin, click Export file and folders.
2. Choose Multi-file export and then Export.
3. This will download a .zip file containing your tokens in JSON format.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Return to Studio

1. Go to your Project Dashboard.
2. Click Upload tokens or drag-and-drop the .zip file into the upload area.

<figure><img src="../.gitbook/assets/Import Tokens.gif" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Review Your Imported Sets

1. Studio will parse the .zip file and create matching sets (e.g., foundation, light, dark).
2. Verify that your sets and tokens appear correctly in the left-hand panel.

<figure><img src="../.gitbook/assets/CleanShot 2025-02-14 at 13.55.01@2x.png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Organizing and Theming Your Tokens

Studio supports theming through the concept of Theme Groups and Theme Options. This allows you to toggle between sets like light and dark, or any other variant (for more information on Themes check out [Features > Themes](../platform/features/themes/)).

The Figma collections will be created as Theme Groups and modes will be created as Theme Options.

1. Open the Theme Panel\
   • In your project, click the Themes tab.
2. Verify that your collections have been created as Theme Groups (e.g., Color Mode, breakpoint)
3. Verify that the modes in your collections have been created as Theme Options under the corresponding Theme Group (e.g., Light and Dark in Color Mode)&#x20;
4. Click on the Theme Option on the left panel to see the sets that are enabled for the Theme Option.
5. Open the Tokens tab on the left panel. \
   • At the bottom of the left-hand panel, you can select which theme is active (e.g., Default + Light or Default + Dark).\
   • This will update the token values displayed in the UI.

<figure><img src="../.gitbook/assets/CleanShot 2025-02-14 at 13.55.12@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
