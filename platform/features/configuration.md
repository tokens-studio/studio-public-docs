# Configuration

The Configuration Module in Studio allows you to generate one or more output files for your tokens—leveraging Style Dictionary under the hood. By creating multiple configurations, you can target different platforms (Android, Web, iOS, etc.) and formats (CSS, XML, JSON). Each configuration can include one or more themes, apply custom transforms, and expand complex tokens. This page walks through how to set up, preview, and manage these configurations.

### Overview

1. Configurations List (Left Pane)
2. &#x20;You can create and manage multiple configurations. For example, you might have one configuration for Android (XML output), another for Web (CSS output), etc.
3. Configuration Details (Center Pane)
   * Name: The name of your configuration (e.g., “Android”, “CSS”, “Web-Mobile”).
   * Included Themes: Select which theme groups (e.g., “Color Mode”, “Breakpoint”) should be processed in this configuration. Studio will generate separate output files for each theme permutation if you use the `{theme}` placeholder in your destination paths.
   * Configuration (Visual or Code): Switch between a user-friendly UI or a code editor. In code view, you can add [Style Dictionary](https://amzn.github.io/style-dictionary/) transforms, custom functions, and advanced filtering.
   * Files & Output: Define multiple files within a single configuration—each with its own output path, transforms, and format.
4. Preview & Output (Right Pane)
   * Preview Theme Permutations: Toggle between each theme combination (e.g., “light” and “dark” in your CSS config) to preview the generated file.
   * Copy or Download: Quickly copy the generated code or download all output files.
   * Code Preview: A read-only preview of the final file (e.g., `.css`, `.xml`, etc.).

### Creating or Editing a Configuration 

1. Add a New Configuration
   * Click Add configuration in the left pane.
   * Give it a Name.
   * Pick themes from the list of theme groups you wish to include. Each chosen group can create multiple permutations (e.g., light/dark, web/mobile).
2. Visual Editor vs. Code View

#### Visual Editor:

* Add an Output File (e.g., `css {theme}.css` or `{theme}.xml`).
* Choose one or more Transform Groups or single transforms (e.g., `name/pascal`, `tokens-studio`).
* Pick the Format (e.g., `css/variables`, `android/resources`).
* Specify the build path (folder where files will be generated).
* Optionally add a prefix to your token names.

#### Code View:

* Exposes the underlying Style Dictionary configuration JSON.
* You can write custom transforms or custom filter functions if needed.
* Refer to the Style Dictionary documentation for examples of advanced usage.

### Expanding Complex Tokens

* Under Expand tokens, select which “composition” tokens (typography, border, shadow, etc.) should be decomposed into separate properties.
* For example, a typography token could be expanded into separate font size, line height, and font family properties.

### Saving

* Click Save changes to persist your configuration. The configuration can now be used in:
* Releases: Generate final output from the Releases page.
* CLI: Pull or generate tokens in your build pipeline (CLI Documentation).

### Previewing and Downloading Output

In the right pane, you’ll see a preview of each generated file:

* Theme Permutations: Use the dropdown to switch among the different permutations created by your selected themes (e.g., `web_light`, `web_dark`, `mobile_light`, `mobile_dark`).
* File Content: Shows the actual code or XML/JSON structure that Style Dictionary produces.
* Copy & Download: Quickly copy the content or download all files at once.

### Deleting a Configuration 

If you no longer need a particular configuration:

1. Select the configuration in the left pane.
2. Scroll to the bottom of the center pane and click Delete config.
3. Confirm the deletion.

### Next Steps

* Run your configuration in the Releases module to package and version your outputs.
* Use our CLI or SDKs to automate token export in your build pipeline.
* Explore Style Dictionary further for custom transforms, attribute definitions, and filter logic.

With the Configuration Module, you can seamlessly produce multiple platform-specific outputs from the same token sets—fully integrated with your themes and custom logic
