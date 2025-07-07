# Import from Tokens Studio for Figma

If you already have design tokens set up in Tokens Studio for Figma plugin, you can easily import them into Studio. Below is an example workflow using the Tokens Studio for Figma plugin.



{% stepper %}
{% step %}
### Open Figma and your design file
{% endstep %}

{% step %}
### Launch the Tokens Studio for Figma plugin
{% endstep %}

{% step %}
### Export your design tokens

1. In the bottom-left of the plugin, click **Export file/folder**.
2. Choose **Multiple files** and then **Export**.
3. This will download a .zip file containing your tokens in JSON format. You can save this anywhere locally on your system.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Upload Tokens to Studio

1. Return to the Tokens Studio app in your browser.
2. Navigate to your Project Dashboard.
3. Using the zip file downloaded above, click the **Upload tokens** or drag-and-drop the zip file into the upload area.

<figure><img src="../.gitbook/assets/Import Tokens.gif" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Reviewing imported tokens and themes&#x20;

1. Studio will parse the .zip file and create matching sets (e.g., foundation, light, dark).
2. Verify that your sets and tokens appear correctly in the left-hand panel.
3. Go to the Themes module on the left panel.
4. Verify that your theme groups and theme options appear correctly.

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

