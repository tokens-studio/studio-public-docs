# Tokens

The Tokens Module in Studio is where you manage and organize your design tokens. This page walks you through the main elements of the interface—navigating sets, creating or uploading tokens, and working within the tokens table. It references other existing sections of the documentation where relevant, so you can easily connect to broader workflows (for example, [Import from Tokens Studio for Figma](../../getting-started/1-playing-with-studio/import-from-tokens-studio-for-figma.md) or [Themes](themes.md)).

### Overview 

When you open the Tokens Module in a Studio project, the layout is divided into two main parts:

1. Left Pane – Displays your token sets and any organizational folders.
2. Right Pane – Shows detailed views for whichever folder or set you have selected—usually referred to as the Tokens Table.

You’ll also find:

* A top bar with search capabilities and actions like Create new set, Upload tokens, or Download tokens.
* A theme selector at the bottom of the left pane, letting you choose which theme context is active (see more in [Themes](themes.md)).

### Navigating Sets and Folders

\
On the left side, you’ll see a structure consisting of Sets and Folders:

* Sets: Contain actual tokens (e.g., colors, typography, spacing). You can rename, duplicate, or delete them.
* Folders: Virtual groupings that help organize multiple sets. They don’t contain tokens directly but let you cluster sets logically.

#### Actions on sets and folders:

* Rename
* Duplicate
* Delete

You’ll also see:

* Last edited timestamp and number of tokens for each set.
* Number of sets inside each folder.

### Creating a New Set

#### To create a new set: 

1. Click Create a new set in the top bar.
2. Give your set a Name and Description (optional).
3. Choose Static set (simple list of tokens) or Graph-based set (tokens can reference each other in more advanced ways).
4. (Optional) Upload an existing set directly from your local JSON files.

For details on uploading tokens from Figma, see [Import from Tokens Studio for Figma](../../getting-started/1-playing-with-studio/import-from-tokens-studio-for-figma.md) or [Import from Figma Variables](../../getting-started/1-playing-with-studio/import-from-figma-variables.md).

### Tokens Table 

Selecting a set from the left pane will switch the right side to Tokens Table view. This view is similar to a spreadsheet, enabling quick, inline editing.\


#### Table Columns

\
Each token row shows:

1. Token Type – e.g., color, typography, dimension, etc.
2. Name – the token’s name (can include hierarchical naming conventions).
3. Value – the token’s raw or referenced value.
4. Resolved Value – the final, resolved value taking references into account.
5. Description – an optional field to clarify the token’s purpose or usage.

#### Inline Editing 

* Enter – switches a cell into edit mode (for simpler tokens like color, dimension, number).
* Space – opens a more detailed editor for more complex tokens (e.g., typography or shadow) where multiple attributes need configuration.

#### Referencing and Resolved Value

\
If a token’s value references another token, you’ll see:\


* A badge indicating whether the reference is valid.
* A Result Value that automatically resolves based on the active theme context.

#### Visualizing Token Flows

\
Each token row has a checkbox on the far left. Selecting one or more tokens enables extra actions. One notable action is Show Token Flow, which provides a visualization of how tokens reference each other—where a token’s value originates and which tokens depend on it.

#### Bulk Actions

\
When you select multiple tokens (by checking rows), you can apply bulk actions such as:\


* Rename
* Duplicate
* Change type
* Change value
* Move
* Delete

#### Folder and File Controls

\
At the top of the Tokens Table, you’ll see breadcrumbs showing your current folder path and file (set) name. You can:\


* Rename the file (set) name in place.
* Download the set as JSON.
* Duplicate the entire set.
* Delete the set.

On the top-right of the table:\


* Filter by token type
* Search tokens by name
* Adjust nesting level (helpful for sets with hierarchical token naming)
* Add Token (also available at the bottom of the table in quick-edit mode)

### Theming Context

\
At the bottom of the left panel, you can pick or create Theme Groups and Theme Options. Choosing a theme changes how references resolve across your tokens.\
To learn more about theming, see [Themes](themes.md).

### Next Steps

* Import tokens from existing sources:
  * [Import from Figma variables](../../getting-started/1-playing-with-studio/import-from-figma-variables.md)
  * [Import from Tokens Studio for Figma](../../getting-started/1-playing-with-studio/import-from-tokens-studio-for-figma.md)
* Configure or refine your themes: [Themes](https://chatgpt.com/g/platform/features/themes.md)
* Leverage advanced references with Graph-based sets

By combining sets, folders, and robust theming, the Tokens Module provides an efficient way to organize your design tokens and keep them updated across different contexts and outputs. If you need more details on advanced usage, head to our [SDKs](../../development/sdks.md) or [CLI](../../development/cli.md) docs to learn about integrating tokens into your codebase.
