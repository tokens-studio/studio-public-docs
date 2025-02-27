# Theme Groups and Theme Options

## Theme Groups and Theme Options

Studio provides a powerful theming system through **Theme Groups** and **Theme Options**. These allow users to manage multiple variations of their design tokens dynamically.

### **Understanding Theme Groups**

A **Theme Group** is a collection of theme options that define different token variations. Theme groups help structure different modes or styles within a design system.

* Each **Theme Group** corresponds to a **collection in Figma**.
* Each **Theme Option** within a Theme Group maps to a **Mode in Figma**.

For example:

* A **Theme Group** called **Color Mode** may contain **Light** and **Dark** options.
* A **Theme Group** called **Breakpoints** may contain options like **320px** and **1440px**.

### **Creating a Theme Group**

1. Navigate to the **Themes** module in Tokens Studio.
2. Click **Create New Theme Group**.
3. Provide a name for your theme group (e.g., "Color Mode").
4. Add one or more theme options (e.g., "Light", "Dark").
5. Click **Save** to confirm.

> **Note**: You can have **more than four theme options**, but only **four will work in Figma** if you're on the **Organization plan** (not Enterprise).

### **Managing Theme Options**

Theme Options represent the different variations within a theme group.

1. Within a **Theme Group**, click **Add Theme Option**.
2. Name the option (e.g., "Light Mode").
3. Provide a description (optional).
4. Click **Save**.

#### **Assigning Token Sets to Theme Options**

Each **Theme Option** can have different token sets assigned to it. This defines which tokens are active when the theme is selected.

* For each **Theme Option**, enable the corresponding token set:
  * **Light Mode** → Assign the **Light Token Set**.
  * **Dark Mode** → Assign the **Dark Token Set**.
* Ensure that your **Foundation Set** is enabled as a source (reference) for both themes.

### **Selecting an Active Theme**

1. At the bottom-left of the Tokens Module interface, locate the **Active Theme Selector**.
2. Choose an active theme (e.g., **Default + Light** or **Default + Dark**).
3. The interface updates to reflect the selected theme’s token values.

### **Deleting a Theme Group or Theme Option**

* To delete a **Theme Group**, go to the Themes panel, select the group, and click **Delete**.
* To remove a specific **Theme Option**, navigate to the group, select the option, and delete it.

### **Use Cases for Theme Groups**

Theme Groups and Options help manage different token variations efficiently. Some common use cases include:

* **Light/Dark Mode** switching.
* **Brand Variants** (e.g., Primary Brand vs. Partner Brands).
* **Breakpoints** for responsive design.
* **Accessibility Themes** (e.g., High Contrast Mode).
