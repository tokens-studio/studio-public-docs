---
description: >-
  Token Flow in Tokens Studio provides a visual way to understand the
  relationships between tokens.
---

# Token flow

### Overview

Token Flow allows you to track references, dependencies, and how tokens are connected across different sets and themes. This feature helps in managing design tokens efficiently and ensuring consistency across your design system.

## Benefits of Token Flow

* **Improved visibility**: Easily see how tokens are structured and related.
* **Efficient debugging**: Quickly identify and resolve issues with token dependencies.
* **Seamless theming**: Understand how token values change dynamically across different themes.



## Accessing Token Flow

{% stepper %}
{% step %}
### **Navigate to the Tokens Module**

<figure><img src="../../.gitbook/assets/CleanShot 2025-02-28 at 19.53.05@2x.png" alt=""><figcaption></figcaption></figure>

Open **Tokens Studio** and go to the **Tokens** module from the left-hand panel. Here, you will see a list of [Token Sets](token-sets.md).
{% endstep %}

{% step %}
### **Select a Token Set**

<figure><img src="../../.gitbook/assets/CleanShot 2025-02-28 at 19.54.37@2x.png" alt=""><figcaption></figcaption></figure>

Click on any **Token Set** to view all the tokens it contains.
{% endstep %}

{% step %}
### **View Token Flow**

Select a token by clicking the checkbox next to it. At the bottom of the screen, the option to open **Token Flow** will appear. Click to open the Token Flow visualization panel and see the references and connections.
{% endstep %}
{% endstepper %}

## Understanding Token Relationships

<figure><img src="../../.gitbook/assets/CleanShot 2025-02-28 at 19.55.58.gif" alt=""><figcaption><p>Opening Token Flow to understand token relationships.</p></figcaption></figure>

Using Token Flow you can:

* **View token references**: See where the token is being referenced across different sets. This is helpful to understand the inheritance model and complexity of references
* **Check dependency paths**: Identify which other tokens rely on the selected token.
* **Explore theme-based variations**: Understand how token values change across different themes. For example, the value of a token may be dependent on

### Example Use Case

1. Select a token, such as a color token.
2. In **Token Flow**, observe:
   * Which other tokens reference it.
   * Whether it pulls values from another token (e.g., from a dark or light theme).
   * How changing the theme affects the resolved token value.
3. If you switch the theme from **Light** to **Dark**, you will see:
   * The reference update from the light token set to the dark token set.
   * The resolved token value changing accordingly.

## Navigating Between Token Sets

* You can click on any referenced token within Token Flow to jump directly to its token set.
* This makes it easier to track how tokens interact across different sets.

<figure><img src="../../.gitbook/assets/CleanShot 2025-02-28 at 20.00.19.gif" alt=""><figcaption></figcaption></figure>
