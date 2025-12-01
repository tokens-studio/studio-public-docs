---
description: >-
  How to move your tokens from the Tokens Studio for Figma Plugin to the Tokens
  Studio platform
---

# Migrating from Tokens Studio for Figma Plugin to the Tokens Studio Platform

## Prerequisites

* A studio account with an active subscription

## Migration Steps

{% stepper %}
{% step %}
### Export your tokens from Tokens Studio for Figma

Within the Tokens Studio for Figma Plugin, click on the "Tools" icon button on the bottom left of the plugin. Within the menu, select "Export to file/folder".

![](<../.gitbook/assets/2025-08-14 at 14.35.39 - Screengrab@2x.png>)&#x20;
{% endstep %}

{% step %}
### Choose "Multiple Files" for the export&#x20;

You'll be given an option to export your tokens to a single file, or multiple files. To maintain a similar structure within Studio, a multiple file export will ensure that your token sets, themes and configuration are maintained.&#x20;

When exported, you will be asked to save a Tokens.zip to your system.

<figure><img src="../.gitbook/assets/2025-08-14 at 14.39.30 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Create a new project with Studio

In your browser, navigate to [https://app.prod.tokens.studio](https://app.prod.tokens.studio/org). Once logged in, create a new project from the dashboard of your organization to upload the tokens to.

<figure><img src="../.gitbook/assets/2025-08-14 at 14.41.40 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Open the upload tokens modal

Once your project has been created, you will be navigated to the dashboard screen of the project. There is a banner on the top of this screen with an button to "Upload tokens".

<figure><img src="../.gitbook/assets/2025-08-14 at 14.43.51 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>

Once clicked, this will open the modal and allow you to upload the zip file from the previous step.

<figure><img src="../.gitbook/assets/2025-08-14 at 14.44.03 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Add the exported zip file to upload

Drag the zip file from your system, or click the modal area to open a file picker.&#x20;

Add the zip file and the upload will begin.

<figure><img src="../.gitbook/assets/2025-08-14 at 14.47.52 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Verify the tokens were uploaded correctly

Once the upload is completed, you can close the modal and see your token sets created with the themes present in the theme switcher below.

<figure><img src="../.gitbook/assets/2025-08-14 at 14.52.10 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## Next steps

Now that you've got your tokens migrated from Figma to Studio, you have a single source of truth that you can use. That means that you can now pull tokens from Studio into your Figma using our companion plugin, or integrate the CLI into your pipelines.

{% content-ref url="../connect-studio-to-figma/using-companion-by-tokens-studio.md" %}
[using-companion-by-tokens-studio.md](../connect-studio-to-figma/using-companion-by-tokens-studio.md)
{% endcontent-ref %}

{% content-ref url="../connect-studio-to-code/tokens-studio-cli.md" %}
[tokens-studio-cli.md](../connect-studio-to-code/tokens-studio-cli.md)
{% endcontent-ref %}

{% content-ref url="integrating-with-github-actions.md" %}
[integrating-with-github-actions.md](integrating-with-github-actions.md)
{% endcontent-ref %}
