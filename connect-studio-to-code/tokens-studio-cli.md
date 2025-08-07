---
description: >-
  Tokens Studio offers an NPM package that you can integrate with your systems.
  This package allows you to connect directly to the Tokens Studio platform and
  pull tokens directly into your project.
---

# Tokens Studio CLI

You may find this useful if you use build pipelines and want to ensure that you have the latest token data in your projects during deployments.

**Prerequisites**:

* [api-keys.md](../settings/api-keys.md "mention")

## **Key Features of the CLI** <a href="#key-features-of-the-cli" id="key-features-of-the-cli"></a>

1. **Current Features:**
   * Pull token sets into local files.
   * Simplify organization and project selection.
2. **Planned Features:**
   * **Watch Mode:** Automatically sync changes from Studio to local files.
   * **Release Artifacts:** Pull releases directly instead of token sets.

## **System Requirements**

* Node v22 or greater is installed [https://nodejs.org/en/download](https://nodejs.org/en/download)

## **Installing the CLI**

{% stepper %}
{% step %}
### Using your terminal, navigate to the directory that you want to connect Studio&#x20;

{% code title="Example of navigating to a directory" %}
```bash
cd ./your-system/projects/my-project
```
{% endcode %}

* Install the  `npm install @tokens-studio/sdk.`
* If you don’t have a `package.json`, initialize it first with `npm init`.
* Ensure that the node.js version installed is v.22 or above.
{% endstep %}

{% step %}
### Initialize your project for NPM

If you don't already have a `package.json` file, you can create one by running `npm init` . This allows npm packages to be installed in the directory.
{% endstep %}

{% step %}
### Install the package

In your terminal, install the package.

```bash
npm install @tokens-studio/sdk --save-dev
```

{% hint style="info" %}
**If you're using a different package manager, the package remains the same. For example:**

Yarn: `yarn add @tokens-studio/sdk --dev`

PNPM: `pnpm install @tokens-studio/sdk --dev`

Bun: `bun add @tokens-studio/sdk --dev`&#x20;
{% endhint %}
{% endstep %}
{% endstepper %}

## Using the CLI

Once installed, you can run commands using `npx tokenstudio`&#x20;

### Available Commands

You can run `npx tokensstudio --help` to view all available commands from the CLI.

```bash
Tokens Studio CLI  2.0.2

Usage:
$ tokensstudio 
   
Commands: 
pull
setup

For more info, run any command with the `--help` flag:
$ tokensstudio --help
$ tokensstudio pull --help
$ tokensstudio setup --help 

Options:
--help       [boolean] Shows an overview of CLI usage
--version    [boolean] Prints NPM version of the CLI
```

## Setting up your project with the CLI

{% hint style="warning" %}
You will need an API key generated from the Tokens Studio platform. If you don't have this available, you can follow [these instructions to generate one](./#creating-an-api-key).
{% endhint %}

Once installed, you will need to configure the CLI to use your Tokens Studio account.&#x20;

{% stepper %}
{% step %}
### In your terminal, run the setup command

`npx tokensstudio setup`
{% endstep %}

{% step %}
### When prompted, enter your API key.

```bash
 Tokens Studio CLI  2.0.2

You did not pass an API key in the environment variables, but you can paste one here.
      You can create an API key in Studio user settings by navigating to a project dashboard 
      and clicking the bottom left menu -> API keys.

               API key: 
```

{% hint style="info" %}
### You can skip the setup step by defined the API KEY as an environment variable when calling the CLI.

```bash
TOKENSSTUDIO_APIKEY=<API_KEY> npx tokensstudio pull
```
{% endhint %}
{% endstep %}

{% step %}
### Select the organization and project

```bash
✔  Done!
         ■ Fetched organizations
         ■ Fetched projects

Select your organisation
Hyma

Select your project
Tokens Zen Garden
```

When successful, a `.tokensstudio.json` file will be created at the root of your project.

<pre class="language-json"><code class="lang-json">{
  "version": "2",
<strong>  "org": "7xxxxxx1-3xx5-4xxx-xxx6-xxxx4axxxxf2",
</strong>  "project": "xxxxfa7d-xxxx-4xxx-xxx2-xxxx0126xxxx",
  "branch": "main",
  "release": "",
  "output": "tokens"
}
</code></pre>
{% endstep %}

{% step %}
### Pull Tokens into your project

In the `.tokensstudio.json` file, edit the **output** property value to be the local project directory where you'd like the tokens to be stored. For example, if your project uses a `src` directory, you would want to change that to `"output": "src/tokens"`\


Use the `pull` command to download the tokens from Tokens Studio to your project.

```bash
npx tokensstudio pull
```

{% code title="Results" %}
```bash
✔  Done!
 ■ Fetched tokensets

✔  Success Found 18 sets with 938 tokens in total.
 ◼   global.json
 ◼   semantic.json
 ◼   comp/button.json
 ◼   comp/list-item.json
 ◼   comp/menu-item.json
 ◼   comp/toggle.json
 ◼   pattern/menu-bar.json
 ◼   pattern/feature.json
 ◼   pattern/card-user.json
 ◼   pattern/card-pricing.json
 ◼   sections/nav.json
 ◼   sections/hero.json
 ◼   sections/features.json
 ◼   sections/team.json
 ◼   sections/pricing.json
 ◼   sections/footer.json
 ◼   theme/light.json
 ◼   theme/dark.json
```
{% endcode %}
{% endstep %}
{% endstepper %}
