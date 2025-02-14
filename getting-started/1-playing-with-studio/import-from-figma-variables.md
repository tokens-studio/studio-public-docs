# Import from Figma variables

If you already have design tokens or variables in Figma, you can easily import them into Tokens Studio. Below is an example workflow using the Tokens Studio for Figma plugin.

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

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Import Figma Variables

1. In the plugin, look for an Import Variables button.
2. Choose whether to convert numbers to dimensions, use rem values, etc.
3. Select the variable sets you want to import and click Import.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

_Tip: You might see collections such as “foundation” or “light” and “dark” in Figma, which will become token sets groups and the modes will become token sets in Tokens Studio ._
{% endstep %}

{% step %}
### Export to a Zip File

1. In the bottom-left of the plugin, click Export file and folders.
2. Choose Multi-file export and then Export.
3. This will download a .zip file containing your tokens in JSON format.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Return to Tokens Studio

1. Go to your Project Dashboard.
2. Click Upload tokens or drag-and-drop the .zip file into the upload area.

<figure><img src="../../.gitbook/assets/Import Tokens.gif" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Review Your Imported Sets

1. Tokens Studio will parse the .zip file and create matching sets (e.g., foundation, light, dark).
2. Verify that your sets and tokens appear correctly in the left-hand panel.

<figure><img src="../../.gitbook/assets/CleanShot 2025-02-14 at 13.55.01@2x.png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Organizing and Theming Your Tokens

Tokens Studio supports theming through the concept of Theme Groups and Theme Options. This allows you to toggle between sets like light and dark, or any other variant (for more information on Themes check out [Features > Themes](../../platform/features/themes.md)).

1. Open the Theme Panel\
   • In your project, click the Themes tab.
2. Create a New Theme Group\
   • For example, name one group Color Mode.\
   • Add Light and Dark as theme options.\
   • Click Save.
3. Assign Token Sets to Theme Options\
   • For each theme option, enable the corresponding token set.\
   • E.g., Light enables the light set, Dark enables the dark set.\
   • Also ensure your foundation set is enabled as the default source of reference for both.
4. Select Active Theme\
   • At the bottom of the left-hand panel, you can select which theme is active (e.g., Default + Light or Default + Dark).\
   • This will update the token values displayed in the UI.

<figure><img src="../../.gitbook/assets/CleanShot 2025-02-14 at 13.55.12@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
