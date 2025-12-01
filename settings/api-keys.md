---
description: >-
  API keys provide a secure way to connect Studio to external platforms like
  Figma. These keys enable seamless integration while ensuring secure
  authentication.
---

# API keys

## Accessing the API Key Page

There are multiple ways to navigate to the **API Keys** page:

### From the Project Dashboard

<figure><img src="../.gitbook/assets/Create API Key Light mode .png" alt=""><figcaption></figcaption></figure>

1. Open your **Project Dashboard**.
2. Click on **Create an API Key** to access the API Key management page.

### From the User Panel

<figure><img src="../.gitbook/assets/CleanShot 2025-02-17 at 12.52.32.png" alt=""><figcaption></figcaption></figure>

1. Locate the **left-side panel** of the interface.
2. Click on the **API Keys** option to navigate directly to the API management page.

### Using a Keyboard Shortcut

<figure><img src="../.gitbook/assets/Create api key with cmd k.gif" alt=""><figcaption></figcaption></figure>

1. Press **Cmd + K** (Mac) or **Ctrl + K** (Windows) to open the **Quick Menu**.
2. Type **"API Key"** in the search bar.
3. Select **Manage API Keys** to be redirected to the API Key page.

***

## Creating a New API Key

{% hint style="danger" %}
🚨 **Important:** Once created, the API key will only be shown **once**. Make sure to copy and store it securely.
{% endhint %}

To generate a new API Key:

{% stepper %}
{% step %}
Navigate to the **API Keys** page.

<figure><img src="../.gitbook/assets/Create API Key Light mode  (1).png" alt=""><figcaption></figcaption></figure>

Click on **Create New Token**&#x20;

<figure><img src="../.gitbook/assets/API Keys page .png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Enter a **name** for your API key.

This should something easily identifiable for future reference.
{% endstep %}

{% step %}
Set the expiration period for the key.

For additional security, you can choose to have the token become non-functional after a set period of time.
{% endstep %}

{% step %}
Set the scope of the key.

<figure><img src="../.gitbook/assets/Create new PAT .png" alt=""><figcaption></figcaption></figure>

Choose the data and actions that users and tools using the token can access and perform.

{% hint style="success" %}
If you're using the [tokens-studio-for-figma-plugin.md](../plugins/tokens-studio-for-figma-plugin.md "mention") or the [companion-by-tokens-studio.md](../plugins/companion-by-tokens-studio.md "mention") plugin, you'll need to enable `project:read` , `project:write` and `actor_tokens:create`
{% endhint %}

| Scope                       | Description                                         |
| --------------------------- | --------------------------------------------------- |
| `me:read`                   | Read account data for the currently logged in user. |
| `organizations:read`        | Read data about the organization                    |
| `organizations:write`       | Update data and settings for the organization       |
| `organizations:admin`       | Administer organization data                        |
| `organizations:user:read`   | Read data regarding the users in an organization    |
| `organizations:user:invite` | Can invite users to an organizations                |
| `organizations:user:write`  | Can update user data in an organization             |
| `projects:read`             | Read project data directly                          |
| `projects:write`            | Update project data                                 |
| `projects:admin`            | Administer Projects                                 |
| `actor_tokens:create`       | Create actor tokens for the user                    |
{% endstep %}
{% endstepper %}

***

## Managing API Keys

* The **API Keys** page displays a list of previously created keys.
* You can **delete** old keys when they are no longer needed.
* For security, API keys **cannot be viewed again** after creation.

<figure><img src="../.gitbook/assets/Peronsal Access Tokens.png" alt=""><figcaption></figcaption></figure>

***

## Using API Keys

* API keys can be used to authenticate connections between **Studio** and **Figma** (or other external platforms).
* They are tied to your **user account**, meaning they grant access to all organizations and projects you are part of.

For more details on using API keys for **Figma integration**, refer to the [Connecting Studio to Figma](../connect-studio-to-figma/) guide.

***

### Security Best Practices

* Store API keys in a **secure password manager**.
* Avoid sharing API keys publicly or committing them to version control.
* Regularly **rotate** keys to maintain security.

***

### Related&#x20;

* [connect-studio-to-figma](../connect-studio-to-figma/ "mention")
* [connect-studio-to-code](../connect-studio-to-code/ "mention")
* [using-tokens-studio-for-figma.md](../connect-studio-to-figma/using-tokens-studio-for-figma.md "mention")
* [using-companion-by-tokens-studio.md](../connect-studio-to-figma/using-companion-by-tokens-studio.md "mention")
