# Themes

## Overview

The **Themes Module** in Studio allows you to configure and manage T**heme groups** and T**heme options**, which directly impact the [**Tokens Module**](../tokens/) and [**Configuration Module**](../configuration.md). This ensures a structured approach to managing design variations such as **light mode, dark mode**, or brand-specific themes.

<figure><img src="../../../.gitbook/assets/Tokens and Themes.png" alt=""><figcaption></figcaption></figure>

## Accessing the Themes Module

1. **Navigate to Themes Module:**
   * From the **left panel**, click on **Themes** to enter the module.
2.  **Understanding the Layout:**

    * The **left panel** displays a list of existing **theme groups** and their corresponding **theme options**.\




    <figure><img src="../../../.gitbook/assets/Themes Module New.png" alt=""><figcaption></figcaption></figure>



    * Each theme option shows:
      * **Number of token sets configured**
      * **Number of variables connected to the option**\


    <figure><img src="../../../.gitbook/assets/Themes Module Options.png" alt=""><figcaption></figcaption></figure>

## Creating and Managing Theme Groups

### **Create a New Theme Group**

* Click on **Create Group**.
* Enter a **name** for the theme group.
* Click **Create** to save.



<figure><img src="../../../.gitbook/assets/Create Theme Group.gif" alt=""><figcaption></figcaption></figure>



### **Adding Theme Options**

* Select a **theme group**.
* Click **Add Option** to create a new theme option.
* Save the changes.\


<figure><img src="../../../.gitbook/assets/Settings Theme Options.gif" alt=""><figcaption></figcaption></figure>

## Configuring Token Sets for Theme Options

1. **Select a Theme Option** from the **left panel**.
2. You will see all available **token sets**.
3. Assign token sets using one of the following states:
   * **Disabled:** The token set is not included in the theme option.
   * **Enabled:** All tokens in the set are included.
   * **Source:** This is primarily for **Figma Variables**, ensuring references between collections remain intact.

<figure><img src="../../../.gitbook/assets/Themes Module Options.png" alt=""><figcaption></figcaption></figure>

### How Themes Reflect in the Tokens Module

* Once you set up **theme groups** and **theme options**, they appear in the **Tokens Module**.
* Located at the **bottom left navigation**, you can see:
  * **Theme Groups** (e.g., Brand, Theme)
  * **Theme Options** (e.g., Light, Dark)

<figure><img src="../../../.gitbook/assets/Themes in Tokens Module.png" alt=""><figcaption></figcaption></figure>

## Themes in the Configuration Page

* Theme groups are used in the **Configuration Page** to ensure **token resolution** functions correctly across themes.s
* When Tokens Studio is **linked to the** [**Companion plugin**](../../../connect-studio-to-figma/using-companion-by-tokens-studio.md) **or** [**Tokens Studio for Figma**](../../../connect-studio-to-figma/using-tokens-studio-for-figma.md), theme groups translates as **Figma Variable collections**.&#x20;
* Theme **options** translate as **Modes** in **Figma Collections**.

### How Themes Reflect as Figma Variables

* Once you connect Studio to Figma via [**Tokens Studio for Figma plugin**](../../../connect-studio-to-figma/using-tokens-studio-for-figma.md) or [**Companion by Tokens Studio**](../../../connect-studio-to-figma/using-companion-by-tokens-studio.md)**,** you can create Figma variables using your design tokens.
* Theme groups are created as Collections in Figma variables (e.g., Brand, Theme).
* Theme options are created as Modes inside the variable Collection (e.g., Light, Dark).\


<figure><img src="../../../.gitbook/assets/CleanShot 2025-02-26 at 21.44.22@2x.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/CleanShot 2025-02-26 at 21.47.27@2x.png" alt=""><figcaption></figcaption></figure>
